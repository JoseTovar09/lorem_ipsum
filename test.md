
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


## button (Falta)
(Se encuentra en el proyecto de components)


## button_container (Falta)
(Se encuentra en el proyecto de components)

## cho_purchase_button

Muestra una linea delgada de color #000000 con opacidad 7% (Se encuentra en el proyecto del SDK)

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



