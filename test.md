
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
Contiene un label con un enlance de link en alguna zona en particular. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| labels              | {CHSDKLabelWithEvent}    | True     | dentro de Label tiene los siguientes parametros:  <br/>`text`: {Rich} <br/>`event`: {Event} <br/>`link_text`: String parte del texto donde va a tener el enlance|

Modelo:
```json
{
  "ui_type": "disclaimer_link",
  "data": {
    "labels": [
      {
        "text": {
          "rich": [
            {
              "type": "text",
              "value": {
                "text": "Ao confirmar, aceita os ",
                "modifier": "faint"
              }
            },
            {
              "type": "text",
              "value": {
                "text": "termos gerais ",
                "modifier": "neutral"
              }
            },
            {
              "type": "text",
              "value": {
                "text": "e as",
                "modifier": "faint"
              }
            }
          ],
          "accessibility": "Ao confirmar, aceita os termos gerais e as"
        },
        "link_text": "termos gerais",
        "event": {
          "type": "open_webview",
          "data": {
            "url": "meli://webview/?url=https://frontend.mercadolibre.com/checkout/v2/credits/terms/particular?site=MLB&bar_color=FFDB15&authentication_mode=required"
          }
        }
      }
    ]
  }
}
```

Visualizacion:

<img width="284" alt="Captura de Pantalla 2022-03-05 a la(s) 4 58 11 p  m" src="https://user-images.githubusercontent.com/88452146/156901402-36210939-966a-4806-b9e5-e9f17ced3e70.png">


## disclaimer 

 Muestra un Label (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| labels              | {Rich}    | False     | texto|
| background          |  [String]   | True     | background del label|

Modelo:
```json
{
  "id": "disclaimer_summary",
  "ui_type": "disclaimer",
  "data": {
    "text": {
      "rich": []
    }
  }
}
```
Visualizacion:

<img width="381" alt="Captura de Pantalla 2022-03-05 a la(s) 5 14 22 p  m" src="https://user-images.githubusercontent.com/88452146/156901590-4082e6ec-a9be-4e89-8163-a3eb57933fab.png">

## outlined_container 

 Muestra un view(contendor) deliniado (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| padding              | CHSDKBrickPadding   | True     | mergenes del view|

Modelo:
```json
{
    "ui_type": "outlined_container",
    "data": {
        "padding": {
            "top": "xxxlarge",
            "left": "large",
            "bottom": "xxxlarge",
            "right": "large"
        }
    }
}
```
Visualizacion:

<img width="371" alt="Captura de Pantalla 2022-03-05 a la(s) 5 28 12 p  m" src="https://user-images.githubusercontent.com/88452146/156901864-574b2cf8-6011-4cd4-bec2-e745dd967f2a.png">


## list_row_with_container 

muestra una fila con imagen, label y un stack debajo de la fila principal (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| asset              | MLBFFloxComponentImageModel   | True     | icono de tipo MLBFFloxComponentImageModel|
| title              | {Rich}   | False     | Texto del label|
| price              | {Rich}   | True     | Texto del precio del label|
| style              | CHSDKListRowWithContainerBrickModifierFactory   | True     | Estilo, quick_selector |
| events              | {events}   | True     | |
| bricks              | {bricks}   | True     | |

Modelo:
```json
{
  "ui_type": "list_row_with_container",
  "data": {
    "padding": {
      "bottom": "large"
    },
    "style": "quick_selector",
    "title": {
      "rich": [],
      "accessibility": "Você tem um cupom de desconto?"
    },
    "asset": {
      "data": {
        "id": "buflo_one_tap_payment_coupon"
      },
      "type": "logo",
      "accessibility": "Você tem um cupom de desconto?"
    },
    "event": {}
  }
}
```
Visualizacion:

<img width="382" alt="Captura de Pantalla 2022-03-05 a la(s) 5 36 51 p  m" src="https://user-images.githubusercontent.com/88452146/156902108-f09b65e7-7e7f-4d28-bffb-54ed68a475ce.png">


## image_label 
muestra una imagen con un label al frente (Se encuentra en el proyecto de Components)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| asset              | MLBFFloxComponentImageModel   | True     | icono de tipo MLBFFloxComponentImageModel|
| text              | {Rich}   | True     | Texto del label|
| modifier              | String Enum   | True     | extended\| reduced\| around\| no_padding\| |

Modelo:
```json
{
  "id": "image_label",
  "ui_type": "image_label",
  "data": {
    "asset": {
      "accessibility": "mo_transferhub_clock",
      "data": {
        "local": "clock"
      },
      "type": "icon"
    },
    "text": {
      "rich": []
    }
  }
}
```
Visualizacion:

<img width="348" alt="Captura de Pantalla 2022-03-05 a la(s) 5 45 51 p  m" src="https://user-images.githubusercontent.com/88452146/156902334-ae7fbff6-d4cd-4da8-8b26-a598455ff7ee.png">


## cho_text_content 
muestra un label sin margenes (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| content              | {Rich}   | False     | Texto del label|

```json
{
  "ui_type": "cho_text_content",
  "data": {
    "content": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "test value"
          }
        }
      ],
      "accessibility": "test value"
    }
  }
}
```

Visualizacion:

<img width="379" alt="Captura de Pantalla 2022-03-05 a la(s) 5 55 50 p  m" src="https://user-images.githubusercontent.com/88452146/156902428-e07dd5a7-59e3-4a08-a012-573d884e0d22.png">


## cho_webview 
muestra un webView  (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| url              | String   | False     | url de la web|
| authenticated              | Bool   | True     | Saber si esta autenticado|

```json
{
  "ui_type": "cho_webview",
  "data": {
    "authenticated": true,
    "url": "https://frontend.mercadolibre.com/checkout/v2/credits/terms/general?site=MLB"
  }
}
```

Visualizacion:

![Simulator Screen Shot - iPhone 12 - 2022-03-05 at 17 56 53](https://user-images.githubusercontent.com/88452146/156902543-ec085003-a337-47dc-b5a7-b1aa37f1fac4.png)


## list_row 
muestra una imagen, icon y un stack, se utiliza en las congrats (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title              | {Rich}   | False     |titulo del texto|
| description         |{Rich}   | True     |Descripcion del texto|
| icon         |CHSDKCongratsFloxImage   | False     |imagen del icono|
| style         |String   | Fasle     ||
| event         |{event}   | Fasle     ||

```json
{
    "ui_type": "list_row",
    "data": {
        "title": {
            "rich": [],
        },
        "style": "selector",
        "event": {}
    }
}
```


## cho_sdk_integrator_image 
Contiene un view con un ImageView (MLBFFloxComponentImageView) - (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| image              | MLBFFloxComponentImageModelData   | True     |imagen|
| accessibility         |String  | True     ||


## cho_sdk_integrator_space 
Contiene un view que cambia su altura utilizado como espacio en blanco - (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| height              | String   | False     |altura del espacio.|


## cho_sdk_one_tap_payment_account_money_with_other_method 
pagar con Account Money con otro metodo de pago. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title              | {Rich}   | False     |Texto del label|
| asset              | MLBFFloxComponentImageModel   | True     |imagen del icono|


```json
{
    "ui_type": "cho_sdk_one_tap_payment_account_money_with_other_method",
    "data": {
      "asset": {
        "data": {
          "id": "mercado-pago-black"
        },
        "type": "logo",
      },
      "title": {
        "rich": []
      }
    },
    "bricks": [
      {
        "ui_type": "switch",
        "data": {
          "checked": true,
          "event": {
          }
        },
        "id": "switch"
      }
    ],
}
```

Visualizacion:

<img width="379" alt="Captura de Pantalla 2022-03-05 a la(s) 6 24 29 p  m" src="https://user-images.githubusercontent.com/88452146/156903103-92740b0e-0126-485b-a05c-0adf7f705cda.png">

## cho_sdk_integrator_row_with_image 
Muetsra una imagen con dos texto al frente.  (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title              | {Rich}   | True     |Texto del primer label|
| description        | {Rich}   | True     |Texto del segundo label|
| image              | MLBFFloxComponentImageModel   | True     |obtiene la imagen|
| fade_anim          | CHSDKFadeAnimationModel   | True     |tipo de animacion al mostrar el componente|

Model: 

```json
{
  "ui_type": "cho_sdk_integrator_row_with_image",
  "data": {
    "image": {
      "data": {
        "url": "https://http2.mlstatic.com/D_691535-MLA29134565196_012019-I.jpg"
      },
      "type": "image"
    },
    "description": {
      "rich": [],
      "accessibility": "Quantidade: 1"
    },
    "fade_anim": {
      "duration": 1500,
      "delay": 0,
      "alpha_from": 0,
      "alpha_to": 1
    },
    "title": {
      "rich": [ ],
      "accessibility": "Item De Teste Fs 9kg"
    }
  }
}
```

Visualizacion:

## cho_sdk_integrator_button 
este brick esta configurado en el proyecto del SDK pero obtiene la data y el view de [button](#button). (Se encuentra en el proyecto del SDK)


## cho_sdk_integrator_card 
es un contendor que tiene un stack y es utilizado en oneTap  (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| padding              | CHSDKBrickPadding   | True     |Margenes del contendor|


## one_tap_main 
Contiene un stack y debajo un View. es utilizado en oneTap  (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| close_event              | {event}   | True     ||
| not_closable              |Bool   | True     ||


## ftu_main 
Tiene el mismo data y view que [one_tap_main](#one_tap_main)  (Se encuentra en el proyecto del SDK)


## cho_sdk_one_tap_modal 
Tiene el mismo data y view que [one_tap_main](#one_tap_main)  (Se encuentra en el proyecto del SDK)

## list_row_with_price 
 lista de items con su precio  (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| hidden              | Bool   | True     ||
| title              |{Rich}   | True     ||
| subtitle              |{Rich}   | True     ||
| description              |{Rich}   | True     ||
| description_event              |{event}   | True     ||
| price              |{Rich}   | True     ||
| full_price              |{Rich}   | True     ||
| style              |String   | True     ||
| modifier              |String   | True     ||
| event              |{event}   | True     ||


```json
{
  "ui_type": "list_row_with_price",
  "data": {
    "padding": {
      "bottom": "large"
    },
    "title": {
      "rich": [],
    },
    "price": {
      "rich": [],
    },
    "modifier": "ellipsize"
  },
}
```
Visualizacion:

<img width="364" alt="Captura de Pantalla 2022-03-05 a la(s) 6 52 06 p  m" src="https://user-images.githubusercontent.com/88452146/156903545-fa838f76-c019-4950-a96e-481f39fab0a3.png">



**input_amount**

