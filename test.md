
- [title_with_action](#title_with_action)
- [separator](#separator)
- [button_container](#button_container)
- [button](#button)
- [cho_purchase_button](#cho_purchase_button)
- [cho_purchase_submit_button](#cho_purchase_submit_button)
- [form](#form)
- [input_text](#input_text)
- [submit_button](#submit_button)
- [cho_stack](#cho_stack)
- [cho_navigation_bar](#cho_navigation_bar)
- [cho_title](#cho_title)
- [separator](#separator)
- [separator](#separator)
- [separator](#separator)
- [separator](#separator)


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

## cho_purchase_submit_button

Muestra un boton con animacion cuando sea seleccionado. Tiene el mismo data que [cho_purchase_button](#cho_purchase_button) (Se encuentra en el proyecto del SDK)


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
| constraints       | {constraints}           | True     |objecto tipo InputTextConstraint. Realiza verificacion|
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


## submit_button

boton para enviar datos del formulario. Tiene el mismo data que el [button](#button). (Se encuentra en el proyecto de Components)
* tiene el objeto Event que es el que contiene la logica para enviar los datos del formulario.

Visualizacion: 

<img width="351" alt="Captura de Pantalla 2022-03-05 a la(s) 3 02 33 p  m" src="https://user-images.githubusercontent.com/88452146/156898427-9481f679-6624-4b05-b94f-aca07bf499aa.png">

## cho_stack

Brick que abre un modal pantalla completa, donde tiene navigation, footer, stackView. (Se encuentra en el proyecto del SDK) y se utiliza en OneTap.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros|
| focus_brick         | {focus_brick}    | True      | objeto focus_brick que tiene como parametros id_brick |

Modelo: 

```json
{
  "ui_type": "cho_stack",
  "data": {
    "focus_brick":{
      "ib_brick": "input_security_code6"
    }
  }
}
```

Visualizacion: 

![Simulator Screen Shot - iPhone 12 - 2022-03-05 at 15 19 10](https://user-images.githubusercontent.com/88452146/156899325-7d208367-9923-4c05-99f6-343a2d480f02.png)



## cho_navigation_bar
Brick que pinta la barra de navegacion. es usada con [cho_stack](#cho_stack) para colocar la navegacion al modal. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros|
| icon         | {icon}    | True      | objeto icon que tiene como parametros type y data |
| event         | {event}    | True      |  |

Modelo: 

```json
{
    "ui_type": "cho_navigation_bar",
    "data": {
        "icon": {
            "type": "icon",
            "data": {
                "local": "back"
            }
        },
        "event": {
            "type": "go_back"
        }
    }
}
```

Visualizacion: 

<img width="390" alt="Captura de Pantalla 2022-03-05 a la(s) 3 25 36 p  m" src="https://user-images.githubusercontent.com/88452146/156899027-552fa609-a86e-47a6-b77d-644147a7da72.png">


## cho_title 

Brick que pinta el titulo. Por lo general es usada para colocar el titulo al modal. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros|
| title               | {rich}           | False     |array obj de tipo Rich|
| subtitle            | {rich}           | False     |array obj de tipo Rich|
| modifier            | String           | True      |string enum que modifca los constraint del titulo. (padded)|

Modelo:

```json
{
  "ui_type": "cho_title",
  "data": {
    "modifier": "padded",
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Prencha os dados para sua nota fiscal"
          }
        }
      ],
      "accessibility": "Prencha os dados para sua nota fiscal"
    },
    "subtitle": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Com estas informações, o vendedor poderá gerar a Nota Fiscal da sua compra."
          }
        }
      ],
      "accessibility": "Com estas informações, o vendedor poderá gerar a Nota Fiscal da sua compra."
    }
  }
}
```

Visualizacion: 

<img width="390" alt="Captura de Pantalla 2022-03-05 a la(s) 3 37 50 p  m" src="https://user-images.githubusercontent.com/88452146/156899285-7d669226-6d4c-440f-9c8a-bd2d11a1e716.png">


## cho_subtitle 

Brick que tiene un label (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parametros |
| subtitle            | {rich}           | False     |array obj de tipo Rich|


## footer_action_container 

Brick para pintar el footer con su contenido. contiene un stack de bricks. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | True     |Objeto que contiene los parametros  title \| total_amount |
| title.              | {rich}           | True     |array obj de tipo Rich|
| total_amount        | {FooterTotalAmountData}     | True     |array obj de tipo FooterTotalAmountData|
| bricks        | [bricks]     | True     |array obj que contiene los bricks que va a mostrar dentro del footer|

Modelo:

```json
{
  "ui_type": "footer_action_container",
  "data": {
    "total_amount": {
      "amount": 1360.23
    }
  },
  "bricks": [
    {
      "ui_type": "submit_button",
      "data": {
        "text": "Continuar",
        "style": "loud"
      }
    }
  ]
}
```
Visualizacion: 

<img width="385" alt="Captura de Pantalla 2022-03-05 a la(s) 3 49 46 p  m" src="https://user-images.githubusercontent.com/88452146/156899723-d588e1c0-1311-422d-baa3-2a38702998d1.png">


## fullscreen_error_with_back 

Muestra la pantalla de error con la navegacion. no tiene Data (Se encuentra en el proyecto del SDK)

## input_card_radio_button 

Muestra un radio Button con un texto y texto con acciones dentro de una card (Se encuentra en el proyecto de Components)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | True     |Objeto que contiene los parametros |
| name             | String           | False     |nombre del radio button|
| value        | []     | False     |Objeto que contiene el valor del radioButton|
| selected        | Bool     | True     |atributo que dice si esta o no seleccionado el radio button|
| title        | {Rich}     | False     |Texto que aparece al lado del radio button.|
| subtitle        | {Rich}    | True     |Texto que aparece a bajo del titulo|
| actions        | [MLBFFloxComponentRadioButtonCardAction]     | True     ||

Modelo:

```json
{
    "ui_type": "input_card_radio_button",
    "data": {
        "name": "shipping_addresses_hub_radio_button_1",
        "value": {"address_id": "1103142906"},
        "selected": true,
        "title": {
            "rich": []
        },
        "subtitle": {
            "rich": [],
            "accessibility": "CP: 1430 - Saavedra, Capital Federal Rosa Martínez - 011152839407"
        },
        "actions": [
            {
                "text": {
                    "rich": [
                        {
                            "type": "text",
                            "value": {
                                "modifier": "neutral",
                                "text": "Mostrar alerta"
                            }
                        }
                    ],
                    "accessibility": "Editar domicilio"
                },
                "event": {
                    "type": "alert",
                    "data": { }
                }
            },
            {
                "text": {
                    "rich": [
                        {
                            "type": "text",
                            "value": {
                                "modifier": "neutral",
                                "text": "Acción sin evento asociado"
                            }
                        }
                    ],
                },
                "event": {
                    "type": "go_to_delivery_instructions",
                    "data": { }
                }
            }
        ]
    }
}
```

Visualizacion: 

<img width="372" alt="Captura de Pantalla 2022-03-05 a la(s) 4 22 19 p  m" src="https://user-images.githubusercontent.com/88452146/156900288-5dc21e23-1901-4640-b944-1ba63cf8849d.png">

## input_card_radio_button_group

Tiene un sctak donde agrupa N [input_card_radio_button](#input_card_radio_button) en una card, No tiene data (Se encuentra en el proyecto de Components)

Visualizacion: 

<img width="379" alt="Captura de Pantalla 2022-03-05 a la(s) 4 51 10 p  m" src="https://user-images.githubusercontent.com/88452146/156901044-2c09f2b1-f5d2-492b-a0fb-4b3eedb35560.png">


## list_container 

Contenedor de lista (Se encuentra en el proyecto de Components).


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title               | {Rich}           | True    |Texto que aparece al lado del radio button.|
| modifier            | String Enum    | True     | separator \| all_separator |
| footer_action       | MLBFFloxComponentLabelFooter    | True     |Footer al final de la lista|


Visualizacion:

<img width="352" alt="Captura de Pantalla 2022-03-05 a la(s) 4 31 14 p  m" src="https://user-images.githubusercontent.com/88452146/156900468-2cb278e2-8605-4de3-9893-16921305309b.png">



## switch 

Contiene un switch (Se encuentra en el proyecto de Components)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| checked               | Bool           | True    |Texto que aparece al lado del radio button.|
| event                 | {event}    | False     | separator \| all_separator |

Modelo:
```json
{
    "ui_type": "switch",
    "data": {
        "checked": false,
        "event": {
            "type": "cho_sdk_one_tap_payment_am_with_om",
            "data":{
                "combine_with_am": true
            }
        }
    }
}
```


Visualizacion:

<img width="100" alt="Captura de Pantalla 2022-03-05 a la(s) 4 39 22 p  m" src="https://user-images.githubusercontent.com/88452146/156900646-c94206b2-acbc-4550-9428-84e2945df7a7.png">

## disclaimer_link 



**input_amount**

