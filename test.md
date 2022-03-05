
- [title_with_action](#title_with_action)
- [separator](#separator)
- [error](#error)


## title_with_action

Muestra dos texto, uno de ellos permite tener una accion. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title               | rich Object      | False    |Objeto que contiene un array Rich.|
| action              | rich Object      | True     |Objeto que contiene un array Rich.|
| event               | event Object     | True     |Objeto que contiene event.|

Modelo:

```json
{
  "ui_type": "title_with_action",
  "data": {
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Primeiro pagamento"
          }
        }
      ],
      "accessibility": "Primeiro pagamento"
    },
    "action": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Alterar"
          }
        }
      ],
      "accessibility": "Alterar"
    },
    "event": {
      "type": "go_to_alter"
    }
  }
}
```

Visualizacion: 

<img width="378" alt="Captura de Pantalla 2022-03-04 a la(s) 6 57 28 p  m" src="https://user-images.githubusercontent.com/88452146/156857551-e4448af3-212b-4a6d-9c1e-61f8a3673630.png">


## separator

Muestra una linea delgada de color #000000 con opacidad 7% (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros del separator|
| hidden              | Bool.            | False     |Boleano que nos dice si mostramos o ocultamos el separador|
| padding             | {CHSDKBrickPadding}| True     |Objeto de tipo CHSDKBrickPadding que contiene los size|

Modelo:

```json
{
    "ui_type": "separator",
    "data" : {
        "hidden" : true,
        "padding": {
            "bottom": "large"
        }
    }
}
```

Visualizacion: 

<img width="389" alt="Captura de Pantalla 2022-03-04 a la(s) 7 07 42 p  m" src="https://user-images.githubusercontent.com/88452146/156858177-89096841-bb3c-40ae-9f8a-9b0f1d224aed.png">

## button_container
Es un brick especial para contener los [button](#button) puede contener N botones. (Se encuentra en el proyecto de Components). 
Contiene los botones con un margen en especial. 

Modelo:

```json
{
    "ui_type": "button_container",
    "data" : {
        "text" : "Botones"
    },
    "bricks": [
      {
        "id": "button1",
        "ui_type": "button",
        "data": {
          "text": "Loud",
          "style": "loud",
          "event": {
            "type": "alert"
          },
          "accessibility": "loud button style"
        }
      }    
    ]
}
```

## button

Diferentes tipos de botones que tambien maneja iconos dentro del boton. (Se encuentra en el proyecto de Components)

* No es necesario que los botones esten dentro de [button_container](#button_container). 
* Tener en cuenta que si los botones no esta dentro de [button_container](#button_container) sus margenes sera toda la pantalla (ancho).


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros del boton|
| text                | String           | False     |texto que se muestra en el boton|
| style               | String Enum      | False     |loud \| quiet \| transparent. Default quiet.<br/>`loud`: Estilo de boton normal<br/>`quiet`: Boton con fondo opaco<br/>`transparent`: Boton con fondo transparante|
| icon                | {icon}           | True      |objeto que contiene: <br/>`id`: id del icono (String) <br/>`orientation`: orientacion del icono (String) left \| rigth  |
| event               | {event}          | False     |objeto que contiene el evento accionar luego de que el boton fue precionado|
| accessibility       | String           | False     ||

Modelo:

```json
{
  "ui_type": "button",
  "data": {
    "text": "Icon left",
    "style": "loud",
    "icon": {
      "id": "download",
      "orientation": "left"
    },
    "event": {
      "type": "alert"
    },
    "accessibility": "Cómo se verá en el resumen"
  }
}
```

Visualizacion: 

<img width="375" alt="Captura de Pantalla 2022-03-05 a la(s) 2 04 54 p  m" src="https://user-images.githubusercontent.com/88452146/156896774-da4e3db1-641b-485a-ad58-985ab3b00869.png">


## cho_purchase_button

Muestra un boton con animacion cuando sea seleccionado. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros del button|
| text                | String           | False     |texto que se muestra en el boton|
| loading_text        | String           | False     |texto que se muestra cuando el boton tiene la animacion|
| max_duration        | Int              | False     |tiempo de duracion de la animacion del boton|
| event               | {event}          | False     |objeto que contiene el evento accionar luego de que el boton fue precionado|
| accessibility       | String           | False     ||

Modelo:

```json
{
    "id": "cho_purchase_button",
    "data": {
        "text": "Confirmar a compra",
        "loading_text": "Já é quase sua!",
        "max_duration": 5.0,
        "event": {
            "type": "split_payment_purchase_confirmed",
            "data": {}
        },
        "accessibility": "Confirmar a compra"
    }
}
```

Visualizacion: 

![ezgif com-gif-maker-15](https://user-images.githubusercontent.com/88452146/156859014-3047a4ae-c31d-4902-b74a-b4a77346e27a.gif)

## cho_purchase_submit_button (Pendiente)

## form (Pendiente)
esta en components

## input_text

Campo de texto con un label en la parte superior. (Se encuentra en el proyecto de Components)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros|
| name                | String           | True      |texto que se muestra en el boton|
| label        | String           | True     |Texto que se muestra en el label. Se encuentra en la parte superior del campo de texto|
| hint        | String              | True     |Texto que muestra en el campo de texto como Hint|
| disabled_text       | String           | True     | |
| constraints       | {constraints}           | True     |objecto tipo InputTextConstraint.|
| attributes       | [attributes]           | True     | Array del objeto attributes que contiene: <br/>`name`: maxLength \| keyboard \| data-mask <br/> Cada uno contiene parametros diferentes (ver code) |
| data_to_fill       | {InputTextBrickDataToFill}           | True     |objecto tipo InputTextBrickDataToFill|
| event_focus       | {event}           | True     ||
| tracks       | {tracks}           | True     ||

Modelo:

```json
{
  "ui_type": "input_text",
  "data": {
    "style": "simple",
    "name": "cpf",
    "label": "CPF",
    "hint": "",
    "attributes": [
      {
        "name": "keyboard",
        "value": "number"
      },
      {
        "name": "data-mask",
        "regex": "^(\\d{3})\\.?(\\d{1,3})?\\.?(\\d{1,3})?-?(\\d{1,2})?$",
        "mask": [
          ".",
          ".",
          "-"
        ]
      }
    ],
    "constraints": {
      "immediate_constraints": [
        {
          "name": "required",
          "value": true,
          "error_message": "REQUIRED"
        }
      ],
      "triggered_constraints": [
        {
          "name": "required",
          "value": true,
          "error_message": "REQUIRED"
        },
        {
          "name": "minLength",
          "value": 4,
          "error_message": "MIN_LENGTH"
        },
        {
          "name": "documentValidation",
          "value": "CPF-MLB",
          "error_message": "DOCUMENT"
        }
      ]
    }
  }
}
```

Visualizacion: 

<img width="352" alt="Captura de Pantalla 2022-03-05 a la(s) 2 34 10 p  m" src="https://user-images.githubusercontent.com/88452146/156898124-9c7cf886-7489-4ae7-bce1-66c9fd06601a.png">




## submit_button (Pendiente)
esta en components

## cho_stack (pendiente)

## cho_navigation_bar (pendiente)

## cho_title (pendiente)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros del button|
| text                | String           | False     |texto que se muestra en el boton|
| loading_text        | String           | False     |texto que se muestra cuando el boton tiene la animacion|
| max_duration        | Int              | False     |tiempo de duracion de la animacion del boton|
| event               | {event}          | False     |objeto que contiene el evento accionar luego de que el boton fue precionado|
| accessibility       | String           | False     ||

Modelo:

```json
{
    "id": "cho_purchase_button",
    "data": {
        "text": "Confirmar a compra",
        "loading_text": "Já é quase sua!",
        "max_duration": 5.0,
        "event": {
            "type": "split_payment_purchase_confirmed",
            "data": {}
        },
        "accessibility": "Confirmar a compra"
    }
}
```

Visualizacion: 

![ezgif com-gif-maker-15](https://user-images.githubusercontent.com/88452146/156859014-3047a4ae-c31d-4902-b74a-b4a77346e27a.gif)



