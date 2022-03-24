# Lista de Bricks CHOSDK - Components - Split

En esta seccion mostramos la lista de los bricks "ui_type" que soportamos en los poryectos CHOSDK, Components y Split en iOS 🍎.

# Modulo Common - SDK

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
- [cho_subtitle](#cho_subtitle)
- [footer_action_container](#footer_action_container)
- [fullscreen_error_with_back](#fullscreen_error_with_back)
- [input_card_radio_button](#input_card_radio_button)
- [input_card_radio_button_group](#input_card_radio_button_group)
- [list_container](#list_container)
- [switch](#switch)
- [disclaimer_link](#disclaimer_link)
- [disclaimer](#disclaimer)
- [outlined_container](#outlined_container)
- [list_row_with_container](#list_row_with_container)
- [image_label](#image_label)
- [cho_text_content](#cho_text_content)
- [cho_webview](#cho_webview)
- [list_row](#list_row)
- [cho_sdk_integrator_image](#cho_sdk_integrator_image)
- [cho_sdk_integrator_space](#cho_sdk_integrator_space)
- [cho_sdk_one_tap_payment_account_money_with_other_method](#cho_sdk_one_tap_payment_account_money_with_other_method)
- [cho_sdk_integrator_row_with_image](#cho_sdk_integrator_row_with_image)
- [cho_sdk_integrator_button](#cho_sdk_integrator_button)
- [cho_sdk_integrator_card](#cho_sdk_integrator_card)
- [one_tap_main](#one_tap_main)
- [ftu_main](#ftu_main)
- [cho_sdk_one_tap_modal](#cho_sdk_one_tap_modal)
- [list_row_with_price](#list_row_with_price)
- [fullscreen_error](#fullscreen_error)
- [generic_container](#generic_container)

# Modulo Payment - SDK
- [one_tap_payment_installments](#one_tap_payment_installments)
- [one_tap_cards_selector](#one_tap_cards_selector)
- [cho_payment_card_container](#cho_payment_card_container)
- [cho_payment_card_medium](#cho_payment_card_medium)
- [cho_sdk_payment_payment_off_card](#cho_sdk_payment_payment_off_card)
- [cho_payment_new_card](#cho_payment_new_card)
- [installments_list_row](#installments_list_row)
- [payment_option_row](#payment_option_row)
- [cho_payment_account_money_card](#cho_payment_account_money_card)
- [cho_payment_default_card](#cho_payment_account_money_card)
- [cho_payment_credits_card](#cho_payment_account_money_card)
- [discount_list_row](#cho_payment_account_money_card)
- [discount_coupon_list_row](#discount_coupon_list_row)
- [discounts_total](#discounts_total)
- [cho_add_coupon_submit_button](#cho_add_coupon_submit_button)
- [cho_payment_consumer_credits_card](#cho_payment_consumer_credits_card)
- [cho_payment_account_money_default_card](#cho_payment_account_money_default_card)
- [cho_sdk_payment_installment_carousel_item](#cho_sdk_payment_installment_carousel_item)
- [cho_sdk_payment_installments_carousel](#cho_sdk_payment_installments_carousel)

# Modulo Review - SDK
- [review_container](#review_container)
- [review_summary_container](#review_summary_container)
- [review_summary_row_title](#review_summary_row_title)
- [review_summary_row_detail](#review_summary_row_detail)
- [review_summary_detail_label](#review_summary_detail_label)
- [review_detail_container](#review_detail_container)
- [review_detail_payment](#review_detail_payment)
- [review_detail_item](#review_detail_item)
- [review_detail_shipping](#review_detail_shipping)




## title_with_action

Muestra dos textos, uno de ellos permite tener una acción. (Se encuentra en el proyecto del SDK)

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
| data                | Object           | False     |Objeto que contiene los parámetros del separator|
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

Visualización: 

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

Diferentes tipos de botones que también maneja iconos dentro del botón. (Se encuentra en el proyecto de Components)

* No es necesario que los botones esten dentro de [button_container](#button_container). 
* Tener en cuenta que si los botones no esta dentro de [button_container](#button_container) sus márgenes serán toda la pantalla (ancho).


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parámetros del botón|
| text                | String           | False     |texto que se muestra en el botón|
| style               | String Enum      | False     |loud \| quiet \| transparent. Default quiet.<br/>`loud`: Estilo de botón normal<br/>`quiet`: Botón con fondo opaco<br/>`transparent`: Botón con fondo transparante|
| icon                | {icon}           | True      |objeto que contiene: <br/>`id`: id del icono (String) <br/>`orientation`: orientación del ícono (String) left \| rigth  |
| event               | {event}          | False     |objeto que contiene el evento accionar luego de que el botón fue precionado|
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

Visualización: 

<img width="375" alt="Captura de Pantalla 2022-03-05 a la(s) 2 04 54 p  m" src="https://user-images.githubusercontent.com/88452146/156896774-da4e3db1-641b-485a-ad58-985ab3b00869.png">


## cho_purchase_button

Muestra un botón con animación cuando sea seleccionado. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parámetros del button|
| text                | String           | False     |texto que se muestra en el botón|
| loading_text        | String           | False     |texto que se muestra cuando el botón tiene la animación|
| max_duration        | Int              | False     |tiempo de duración de la animación del botón|
| event               | {event}          | False     |objeto que contiene el evento accionar luego de que el botón fue precionado|
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

Visualización: 

![ezgif com-gif-maker-15](https://user-images.githubusercontent.com/88452146/156859014-3047a4ae-c31d-4902-b74a-b4a77346e27a.gif)

## cho_purchase_submit_button

Muestra un botón con animación cuando sea seleccionado. Tiene el mismo data que [cho_purchase_button](#cho_purchase_button) (Se encuentra en el proyecto del SDK)


## form (Pendiente)
esta en components

## input_text

Campo de texto con un label en la parte superior. (Se encuentra en el proyecto de Components)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parámetros|
| name                | String           | True      |texto que se muestra en el botón|
| label        | String           | True     |Texto que se muestra en el label. Se encuentra en la parte superior del campo de texto|
| hint        | String              | True     |Texto que muestra en el campo de texto como Hint|
| disabled_text       | String           | True     | |
| constraints       | {constraints}           | True     |objeto tipo InputTextConstraint. Realiza verificación|
| attributes       | [attributes]           | True     | Array del objeto attributes que contiene: <br/>`name`: maxLength \| keyboard \| data-mask <br/> Cada uno contiene parámetros diferentes (ver code) |
| data_to_fill       | {InputTextBrickDataToFill}           | True     |objeto tipo InputTextBrickDataToFill|
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

Visualización: 

<img width="352" alt="Captura de Pantalla 2022-03-05 a la(s) 2 34 10 p  m" src="https://user-images.githubusercontent.com/88452146/156898124-9c7cf886-7489-4ae7-bce1-66c9fd06601a.png">


## submit_button

botón para enviar datos del formulario. Tiene el mismo data que el [button](#button). (Se encuentra en el proyecto de Components)
* tiene el objeto Event que es el que contiene la lógica para enviar los datos del formulario.

Visualización: 

<img width="351" alt="Captura de Pantalla 2022-03-05 a la(s) 3 02 33 p  m" src="https://user-images.githubusercontent.com/88452146/156898427-9481f679-6624-4b05-b94f-aca07bf499aa.png">

## cho_stack

Brick que abre un modal pantalla completa, donde tiene navigation, footer, stackView. (Se encuentra en el proyecto del SDK) y se utiliza en OneTap.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parámetros|
| focus_brick         | {focus_brick}    | True      | objeto focus_brick que tiene como parámetros id_brick |

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

Visualización: 

![Simulator Screen Shot - iPhone 12 - 2022-03-05 at 15 19 10](https://user-images.githubusercontent.com/88452146/156899325-7d208367-9923-4c05-99f6-343a2d480f02.png)



## cho_navigation_bar
Brick que pinta la barra de navegación. Es usada con [cho_stack](#cho_stack) para colocar la navegación al modal. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parámetros|
| icon         | {icon}    | True      | Objeto icon que tiene como parámetros type y data |
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

Visualización: 

<img width="390" alt="Captura de Pantalla 2022-03-05 a la(s) 3 25 36 p  m" src="https://user-images.githubusercontent.com/88452146/156899027-552fa609-a86e-47a6-b77d-644147a7da72.png">


## cho_title 

Brick que pinta el titulo. Por lo general es usada para colocar el titulo al modal. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| data                | Object           | False     |Objeto que contiene los parámetros|
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

Visualización: 

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

Model: 

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

## fullscreen_error 
Muestra la pantalla de error con la navegacion. no tiene Data (Se encuentra en el proyecto del SDK)

Visualizacion:

<img width="387" alt="Captura de Pantalla 2022-03-23 a la(s) 8 05 23 p  m" src="https://user-images.githubusercontent.com/88452146/159821617-d994839f-1a07-4762-8f6c-54d659c37562.png">


## generic_container 
Contiene un view con stackView, la cual se le puede cambiar el background, padding y addFadeAnimation (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| background          | String           | True     ||
| fade_anim           |CHSDKFadeAnimationModel   | True     ||

Model: 

```json
{
  "id": "container",
  "ui_type": "generic_container",
  "data": {
    "padding": {
      "left": "large",
      "bottom": "xlarge",
      "right": "large"
    },
    "background": "gray-040",
    "fade_anim": {
      "duration": 500,
      "delay": 2000,
      "alpha_from": 1,
      "alpha_to": 0.2
    }
  }
}
```

## one_tap_payment_installments 
Contiene un view con stackView, donde tiene label titulo, amount, informacion. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||
| installment_quantity           |MLBFFloxComponentLabel   | True     ||
| total_amount           |MLBFFloxComponentLabel   | True     ||
| total_amount_sidenote           |MLBFFloxComponentLabel   | True     ||
| additional_info           |MLBFFloxComponentLabel   | True     ||
| tracking           |[AnyHashable: Any]   | True     ||
| event           |FloxEvent   | True     ||
| style           |String   | True     ||

Model: 

```json
{
  "ui_type": "one_tap_payment_installments",
  "data": {
    "padding": {
      "top": "medium",
      "left": "large"
    },
    "title": {
      "rich": [
      ]
    },
    "event": {},
    "total_amount": {
      "rich": [
      ]
    }
  }
}
```

Visualizacion:

<img width="390" alt="Captura de Pantalla 2022-03-23 a la(s) 4 41 28 p  m" src="https://user-images.githubusercontent.com/88452146/159801580-af2760ff-f428-47ad-a8f5-c103c618759e.png">


## one_tap_cards_selector 
Contiene un colectionView con su pageControl. la cual muestra el carrosel de tipos de pagos. No tiene Data. (Se encuentra en el proyecto del SDK)

Model: 

```json
{
  "ui_type": "one_tap_cards_selector",
}
```

Visualizacion:

<img width="394" alt="Captura de Pantalla 2022-03-23 a la(s) 4 53 40 p  m" src="https://user-images.githubusercontent.com/88452146/159802672-228fc33f-c187-4044-8c84-f4a34f5e5f51.png">


## cho_payment_card_container 
Contiene un view (Se encuentra en el proyecto del SDK) (Deprecate?)


## cho_payment_card_medium 
View que contiene la card del metodo de pago. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| full_name          | String           | True     ||
| numbers           |String   | True     |True|
| message           |[AnyHashable: Any]   | True     ||
| selected           |Bool   | True     ||
| background_gradient    |  [String] | True     ||
| tracking           |[AnyHashable: Any]   | True     ||
| on_swipe_events           |CHSDKSwipeCardEventHandler  | True     ||

Model:
```json
{
  "ui_type": "cho_payment_card_medium",
  "data": {
    "full_name": "FUND PRUEBA",
    "issuer_icon": "https://mobile.mercadolibre.",
    "background_color": "#2561C0",
    "on_swipe_events": [
    {}
    ],
    "font_color": "#F5F5F5",
    "bank_icon": "",
    "numbers": "**** 0004",
    "font_type": "light",
    "selected": true
  },
  "id": "one_tap_payment_card_visa_credit_card_25_9033034313"
}
```

Visualizacion:

<img width="369" alt="Captura de Pantalla 2022-03-23 a la(s) 5 09 31 p  m" src="https://user-images.githubusercontent.com/88452146/159804344-1e0d0e15-4a65-405b-9465-02fd0b6b375d.png">

## cho_sdk_payment_payment_off_card 
Contiene una imagen/icon y alfrente un stackView donde solo se agrega un label. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| icon          | CHSDKCongratsFloxImage           | False     ||
| title           |MLBFFloxComponentLabel   | False     ||
| selected           |Bool   | True     ||
| subtitle           |MLBFFloxComponentLabel   | True     ||

Model:

```json
{
    "ui_type": "cho_sdk_payment_payment_off_card",
    "data": {
        "icon": {
        },
        "title": {
            "rich": [
                
            ],
        },
        "on_swipe_events": [],
        "selected": false,
        "subtitle": {
            "rich": [
            ]
        }
    }
}
```


Visualizacion:

<img width="375" alt="Captura de Pantalla 2022-03-23 a la(s) 5 22 51 p  m" src="https://user-images.githubusercontent.com/88452146/159805956-a0eddc58-b48d-4dfb-bc3b-d78df6a093d8.png">

## cho_payment_new_card 
Elemento para agregar una nueva tarjeta. Contiene una imagen/icon y alfrente un stackView donde solo se agrega un label y alfrente contine un icon "chebron_blue". (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| icon          | String           | False     ||
| title           |MLBFFloxComponentLabel   | False     ||
| style           |String   | True     ||
| event           |FloxEvent   | True     ||
| subtitle           |MLBFFloxComponentLabel   | True     ||

Model:

```json
{
  "ui_type": "cho_payment_new_card",
  "data": {
    "icon": "buflo_one_tap_payment_method_credit-card",
    "title": {
      "rich": [
      ],
    },
    "event": {
      "type": "cho_payment_add_new_card",
      "data": {
        }
    }
  }
}
```

## installments_list_row 
Muestra una lista de cuotas, con su precio y detalle. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| quantity          | MLBFFloxComponentLabel           | False     ||
| installment_amount           |MLBFFloxComponentLabel   | False     ||
| total_amount           |MLBFFloxComponentLabel   | True     ||
| selected           |String   | True     ||
| discounts           |[[AnyHashable: Any]]   | True     ||
| tracking           |[AnyHashable: Any]   | True     ||
| on_tap_event           |FloxEvent   | True     ||

Model:

```json
{
  "ui_type": "installments_list_row",
  "data": {
    "selected": "true",
    "quantity": {
      "rich": [
      ]
    },
    "installment_amount": {
      "rich": [
      ]
    },
    "total_amount": {
      "rich": [
      ]
   },
    "discounts": [
      {
        "style": "pill",
        "rich": [
        ]
      },
      {
        "style": "plain",
        "rich": [
        ]
      }
    ]
  }
}
```

Visualizacion:

<img width="382" alt="Captura de Pantalla 2022-03-23 a la(s) 5 38 39 p  m" src="https://user-images.githubusercontent.com/88452146/159807748-fdcc46ff-6e4b-464a-882e-db081c367007.png">

## payment_option_row 
Muestra una lista de opciones de pago (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||
| description           |MLBFFloxComponentLabel   | True     ||
| icon           |CHSDKCongratsFloxImage   | False     ||
| style           |String   | True     ||
| event           |FloxEvent   | True     ||

Model:

```json
{
    "ui_type": "payment_option_row",
    "id": "pay_point_rapipago",
    "data": {
        "event": {},
        "title": {
            "rich": [
            ]
        },
        "icon": {
            "accessibility": "rapipago",
            "data": {
                "id": "buflo_payment_medio-off_rapipago2"
            },
            "type": "logo"
        }
    }
}
```
Visualizacion:

<img width="378" alt="Captura de Pantalla 2022-03-23 a la(s) 5 49 00 p  m" src="https://user-images.githubusercontent.com/88452146/159808945-ae3978f1-b739-4da0-af6c-d56a875a3126.png">


## cho_payment_account_money_card 
Muestra la card de account Money (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| enabled          | Bool           | True     ||
| full_name           |String   | True     ||
| numbers           |String   | True     ||
| message           |[AnyHashable: Any]   | True     ||
| on_swipe_events           |CHSDKSwipeCardEventHandler   | True     ||
| selected           |Bool   | True     ||

Model:

```json
{
  "ui_type": "cho_payment_account_money_card",
  "data": {
    "message": {
      "rich": [
      ],
    },
    "on_swipe_events": [],
    "selected": false,
    "enabled": true
  },
}
```

Visualizacion:

<img width="362" alt="Captura de Pantalla 2022-03-23 a la(s) 5 53 25 p  m" src="https://user-images.githubusercontent.com/88452146/159809371-0534b9c4-964e-40e0-8115-8d93eb868652.png">


## cho_payment_default_card 
Contiene una imagen/icon y alfrente un stackView donde solo se agrega un label y alfrente contine un icon "chebron_blue". (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| icon          | String           | False     ||
| title           |MLBFFloxComponentLabel   | False     ||
| style           |String   | True     ||
| event           |FloxEvent   | True     ||

Model:

```json
{
  "ui_type": "cho_payment_default_card",
  "data": {
    "icon": "buflo_one_tap_payment_method_pix",
    "title": {
      "rich": [
      ]
    },
    "on_swipe_events": [],
    "selected": false,
    "subtitle": {
      "rich": [
      ]
    }
  }
}
```

Visualizacion:

<img width="364" alt="Captura de Pantalla 2022-03-23 a la(s) 5 58 53 p  m" src="https://user-images.githubusercontent.com/88452146/159810074-93d14ef7-9f68-41c2-a809-122b73ad02ad.png">


## cho_payment_credits_card 
Muestra la card de la opcion de pago Credits. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| enabled          | Bool           | True     ||
| full_name           |String   | True     ||
| numbers           |String   | True     ||
| message           |[AnyHashable: Any]   | True     ||
| background_gradient           |String   | False     ||
| issuer_icon           |String   | False     ||

Model:

```json
{
  "ui_type": "cho_payment_credits_card",
  "data": {
     "issuer_icon": "cho_split_buflo_payment_method_credits",
     "background_gradient": [
        "#00BB99",
        "#00A9D1"
     ]
   }
}
```

Visualizacion:

<img width="375" alt="Captura de Pantalla 2022-03-23 a la(s) 6 03 33 p  m" src="https://user-images.githubusercontent.com/88452146/159810582-0cf748c6-2106-469d-a7e7-1121033abe1b.png">



## discount_list_row 
Muestra una lista con la informacion del descuento, con su valor al frente. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| discount          | CHSDKTextPillData           | False     ||
| subtitle           |MLBFFloxComponentLabel   | False     ||
| price           |MLBFFloxComponentLabel   | False     ||

Model:

```json
{
    "ui_type": "discount_list_row",
    "data": {
        "discount": {
            "style": "pill",
            "rich": [
            ]
        },
        "subtitle": {
            "rich": [
            ]
        },
        "price": {
            "rich": [
            ]
        }
    }
}
```

Visualizacion:

<img width="374" alt="Captura de Pantalla 2022-03-23 a la(s) 6 33 45 p  m" src="https://user-images.githubusercontent.com/88452146/159813417-cad80dfa-98d9-44d5-96e5-fa9897aeb167.png">


## discount_coupon_list_row 
Muestra el cupo de descuento (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | True     ||
| subtitle           |MLBFFloxComponentLabel   | True     ||
| price           |MLBFFloxComponentLabel   | False     ||
| action_title           |MLBFFloxComponentLabel   | True     ||
| disabled           |Bool   | True     ||
| event           |FloxEvent   | True     ||


## discounts_total 
Muestra un titulo y al frente su precio (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||
| price           |MLBFFloxComponentLabel   | False     ||

Model:

```json
{
    "ui_type": "discounts_total",
    "data": {
        "title": {
            "rich": [
            ]
        },
        "price": {
            "rich":[
            ]
        }
    }
}
```

Visualizacion:

<img width="390" alt="Captura de Pantalla 2022-03-23 a la(s) 6 40 07 p  m" src="https://user-images.githubusercontent.com/88452146/159814020-bb8973a4-d655-401f-a790-d35efe0ef2d7.png">


## cho_add_coupon_submit_button 
Muestra  un boton para aplicar el cupon ingresado.  (Se encuentra en el proyecto del SDK)

Tiene la misma data que [cho_purchase_button](#cho_purchase_button)

Model:

```json
{
    "ui_type": "cho_add_coupon_submit_button",
    "data": {
        "padding": {
            "top": "§",
            "left": "none",
            "right": "none"
        },
        "text": "Aplicar cupón",
        "event": {
            "type": "coupon_entered"
        },
        "accessibility": "Aplicar cupón",
        "max_duration": 30,
        "loading_text": "¡Ya casi tienes tu descuento!"
    }
}
```

Visualizacion:

<img width="375" alt="Captura de Pantalla 2022-03-23 a la(s) 6 44 24 p  m" src="https://user-images.githubusercontent.com/88452146/159814427-71f1d8e7-2442-410d-acb4-cea3e8e315aa.png">


## cho_payment_consumer_credits_card 
Muestra la card de CustomerCredits con informacion y label con accion.  (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| full_name           |String   | True     ||
| numbers           |String   | True     ||
| message           |[AnyHashable: Any]   | True     ||
| icon           |String   | False     ||
| title           |MLBFFloxComponentLabel   | False     ||
| subtitle           |MLBFFloxComponentLabel   | True     ||
| selected           |Bool   | True     ||
| event           |FloxEvent   | True     ||

Model:

```json
{
  "ui_type": "cho_payment_consumer_credits_card",
  "data": {
    "icon": "buflo_payment_method_mercado-credito",
    "title": {
      "rich": [
      ],
      "accessibility": "Mercado Crédito"
    },
    "event": {
      "type": "go_to_consumer_credits_details",
      "data": {}
    },
    "on_swipe_events": [ ],
    "selected": true,
    "subtitle": {
      "rich": [
      ]
    }
  },
}
```

Visualizacion:

<img width="380" alt="Captura de Pantalla 2022-03-23 a la(s) 6 47 21 p  m" src="https://user-images.githubusercontent.com/88452146/159814688-7b0ab60c-ea45-4b63-a251-2a4aeab7c5e3.png">


## cho_payment_account_money_default_card 
Muestra la card de MercadoPago (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| full_name           |String   | True     ||
| numbers           |String   | True     ||
| message           |[AnyHashable: Any]   | True     ||
| background_gradient           |[String]   | True     ||
| logo_icon           |String   | True     ||
| overlay_image_icon           |String   | True     ||
| on_swipe_events           |[AnyHashable]   | True     ||
| selected           |Bool   | True     ||

Model:

```json
{
  "ui_type": "cho_payment_account_money_default_card",
  "id": "cho_payment_account_money_default_card",
  "data": {}
}
```

Visualizacion:

<img width="380" alt="Captura de Pantalla 2022-03-23 a la(s) 6 52 56 p  m" src="https://user-images.githubusercontent.com/88452146/159815174-2ca9b29b-0188-4a28-aa69-46c22b13e223.png">

## cho_sdk_payment_installment_carousel_item 
Muestra el componente dentro de un carrusel. el componente contiene, numero de cuota con su precio e informacion. (Se encuentra en el proyecto del SDK)
Se utiliza dentro [cho_sdk_payment_installments_carousel](#cho_sdk_payment_installments_carousel)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| quantity          | MLBFFloxComponentLabel           | False     ||
| installment_amount           |MLBFFloxComponentLabel   | False     ||
| additional_info           |MLBFFloxComponentLabel   | True     ||
| selected           |Bool   | True     ||
| event           |FloxEvent   | True     ||

Model:

```json
{
  "ui_type": "cho_sdk_payment_installment_carousel_item",
  "data": {
    "quantity": {
      "rich": [
      ]
    },
    "event": {
    },
    "installment_amount": {
      "rich": [
      ]
    },
    "selected": true
  },
}
```

Visualizacion:

<img width="389" alt="Captura de Pantalla 2022-03-23 a la(s) 6 57 21 p  m" src="https://user-images.githubusercontent.com/88452146/159815562-2ccdbd5a-40ac-4f35-8299-70dbd011c0ac.png">


## cho_sdk_payment_installments_carousel 
Carrosel de cuotas de pago. Contiene un collectionView, label y imagen que contiene el componente [cho_sdk_payment_installment_carousel_item](#cho_sdk_payment_installment_carousel_item)  (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| hidden          | Bool           | True     ||
| current_state           |String   | True     ||
| error_state           |[String: Any]   | True     ||

Model:

```json
{
    "ui_type": "cho_sdk_payment_installments_carousel",
    "data": {
        "hidden": false,
        "padding": {
            "top": "large",
            "left": "large",
            "bottom": "large"
        }
    },
    "bricks": [{}]
}
```

Visualizacion:

<img width="389" alt="Captura de Pantalla 2022-03-23 a la(s) 7 07 21 p  m" src="https://user-images.githubusercontent.com/88452146/159816477-f9047d80-989c-4b2b-a5b8-40ee7003c890.png">


## review_container 
Contiene un stackView dentro de un ScrollView. Es el container principal para la **Review** (Se encuentra en el proyecto del SDK)

- stackView.axis = .vertical
- stackView.distribution = .equalSpacing
- No tiene DATA


## review_summary_container 
Contiene un stackView (Se encuentra en el proyecto del SDK)

- No tiene DATA
- backgroundColor = ml_meli_light_yellow

## review_summary_row_title 
Muestra un titulo centrado (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||

Model:

```json
{
  "id": "review_summary_row_title",
  "ui_type": "review_summary_row_title",
  "data": {
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Confirme a sua compra"
          }
        }
      ],
      "accessibility": "Confirme a sua compra"
    }
  }
}
```

Visualizacion:

<img width="388" alt="Captura de Pantalla 2022-03-23 a la(s) 7 26 37 p  m" src="https://user-images.githubusercontent.com/88452146/159818256-43c3df31-042b-4c2c-aa7d-2803494a251e.png">

## review_summary_row_detail 
Muestra dos label. uno en cada lado de la pantalla (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| primary_text          | MLBFFloxComponentLabel           | True     ||
| secondary_text           |MLBFFloxComponentLabel   | True     ||
| alternative_secondary_text           |MLBFFloxComponentLabel   | True     ||
| modifier           |String   | True     ||

Model:

```json
{
    "ui_type": "review_summary_row_detail",
    "data": {
        "primary_text": {
            "rich": [
            ]
        },
        "secondary_text": {
            "rich": [
            ]
        }
    }
}
```

Visualizacion:

<img width="390" alt="Captura de Pantalla 2022-03-23 a la(s) 7 32 53 p  m" src="https://user-images.githubusercontent.com/88452146/159818657-33b79df9-5fd6-49c7-80a6-8f571364577f.png">


## review_summary_detail_label 
Muestra una lista de cuotas, con su precio y detalle. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||

Model:

```json
{
    "ui_type": "review_summary_detail_label",
    "data": {
        "title": {
            "rich": [
            ]
        },
        "padding": {
            "top": "medium"
        }
    }
}
```

Visualizacion:

<img width="375" alt="Captura de Pantalla 2022-03-23 a la(s) 7 37 00 p  m" src="https://user-images.githubusercontent.com/88452146/159818988-559b9c98-60c2-4534-961a-5cbb26dcf9af.png">


## review_detail_container 
Contiene un StackView, se utilizar como contendor para los bricks dentro del detalle de la **Review** (Se encuentra en el proyecto del SDK)

- No tiene DATA.
- backgroundColor = ml_meli_white

Visualizacion:

<img width="371" alt="Captura de Pantalla 2022-03-23 a la(s) 7 40 29 p  m" src="https://user-images.githubusercontent.com/88452146/159819386-53d3814a-49ac-4ce4-be00-eb2de1644f41.png">


## review_detail_payment 
Muestra el detalle del metodo de pago en la **Review** . (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| quantity          | MLBFFloxComponentLabel           | False     ||
| installment_amount           |MLBFFloxComponentLabel   | False     ||

Model:

```json
{
    "ui_type": "review_detail_payment",
    "data": {
        "icon": {
            "accessibility": "Pix",
            "data": {
                "id": "buflo_one_tap_payment_method_pix"
            },
            "type": "logo"
        },
        "header_title": {
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
        "primary_title": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Pix"
                    }
                }
            ],
            "accessibility": "Pix"
        },
        "secondary_title": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Você paga "
                    }
                },
                {
                    "type": "price",
                    "value": {
                        "symbol": "R$",
                        "fraction": "500",
                        "decimal_separator": ",",
                        "cents": "78"
                    }
                }
            ],
            "accessibility": "Você paga R$ 500"
        },
        "description": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "No podemos reservarte stock hasta que el pago sea aprobado. ¡No pierdas tiempo!"
                    }
                }
            ],
            "accessibility": "No podemos reservarte stock hasta que el pago sea aprobado. ¡No pierdas tiempo!"
        }
    }
}
```

Visualizacion:

<img width="387" alt="Captura de Pantalla 2022-03-23 a la(s) 7 41 35 p  m" src="https://user-images.githubusercontent.com/88452146/159819469-d133843e-3019-4724-9f58-0d4eb4b9a489.png">


## review_detail_item 
Muestra informacion del item/producto. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| primary_title          | MLBFFloxComponentLabel           | True     ||
| secondary_title           |MLBFFloxComponentLabel   | True     ||
| disclaimer           |MLBFFloxComponentLabel   | True     ||
| icon           |CHSDKCongratsFloxImage   | True     ||

Model:

```json
{
    "ui_type": "review_detail_item",
    "id": "review_detail_item",
    "data": {
        "icon": {
            "data": {
                "url": "http://http2.mlstatic.com/D_956736-MLA43784134096_102020-I.jpg"
            },
            "type": "image"
        },
        "primary_title": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "St: Item Test Me2"
                    }
                }
            ],
            "accessibility": "St: Item Test Me2"
        },
        "secondary_title": {
            "rich": [
            ]
        },
        "disclaimer": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Chegará entre os dias 24 e 29 set. no seu endereço"
                    }
                }
            ]
        }
    }
}
```

Visualizacion:

<img width="358" alt="Captura de Pantalla 2022-03-23 a la(s) 7 44 35 p  m" src="https://user-images.githubusercontent.com/88452146/159819707-67f5fac7-b197-4848-96aa-588e8014763d.png">


## review_detail_shipping 
Muestra informacion del envio. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| quantity          | MLBFFloxComponentLabel           | False     ||
| installment_amount           |MLBFFloxComponentLabel   | False     ||

Model:

```json
{
    "ui_type": "review_detail_shipping",
    "id": "review_detail_shipping",
    "data": {
        "icon": {
            "accessibility": "buflo_reference_ship-direccion",
            "data": {
                "id": "buflo_reference_ship-direccion"
            },
            "type": "logo"
        },
        "primary_title": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "SANTO CRISTO SN"
                    }
                }
            ]
        },
        "secondary_title": {
            "rich": [
            ]
        }
    }
}
```

Visualizacion:

<img width="334" alt="Captura de Pantalla 2022-03-23 a la(s) 7 48 26 p  m" src="https://user-images.githubusercontent.com/88452146/159820070-0c0adc29-810f-483f-91c8-0d65b1f474f6.png">



## main 
Contiene un stackview dentro de un scrollView. Es el contenedor principal de la **Congrats** (Se encuentra en el proyecto del SDK)

- No tiene DATA

Model:

```json
{
  "ui_type": "main",
  "bricks": []
}
```


## body_congrats 
Contiene un stackview. Es el Contendor body donde tiene las card de informacion del pago y del item (Se encuentra en el proyecto del SDK)

- No tiene DATA

Model:

```json
{
  "ui_type": "body_congrats",
  "bricks": []
}
```
Visualizacion:

<img width="379" alt="Captura de Pantalla 2022-03-24 a la(s) 9 04 10 a  m" src="https://user-images.githubusercontent.com/88452146/159933588-ee8c6ac8-7928-4907-81c8-7df3980640ba.png">


## card 
Muestra una card, que contiene un stackView de elementos. (Se encuentra en el proyecto del SDK)

- contiene bricks.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| style          | String           | True     ||
| tracking           |[AnyHashable: Any]   | True     ||

Model:

```json
{
  "ui_type": "card",
  "bricks": []
}
```

Visualizacion:

<img width="376" alt="Captura de Pantalla 2022-03-24 a la(s) 9 07 23 a  m" src="https://user-images.githubusercontent.com/88452146/159934274-41c08ef0-3c3d-417d-96ac-7b09b7b89809.png">


## card_information 
Muestra en la informacion del envio del producto. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||
| description           |MLBFFloxComponentLabel   | True     ||
| epigraph           |[[AnyHashable: Any]]   | True     ||
| disclaimer           |MLBFFloxComponentLabel   | True     ||
| keyword           |MLBFFloxComponentLabel   | True     ||
| asset           |MLBFFloxComponentImageModel   | False     ||
| modifier           |String   | True     ||

Model:

```json
{
    "ui_type": "card_information",
    "data": {
        "title": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Envio para rua de test 111"
                    }
                }
            ]
        },
        "disclaimer": {
            "rich": [
            ]
        },
        "modifier": "ellipsis",
        "description": {
            "rich": [
            ]
        },
        "asset": {
            "type": "icon",
            "data": {
                "id": "buflo_congrats_information_shipping"
            }
        }
    }
}
```

Visualizacion:

<img width="346" alt="Captura de Pantalla 2022-03-24 a la(s) 9 20 24 a  m" src="https://user-images.githubusercontent.com/88452146/159936856-4e115675-9b33-4be1-b2c3-6af0f586ed1d.png">


## banner_congrats 
Muestra en la parte superior la informacion de la **Congrats**.   (Se encuentra en el proyecto del SDK)

- Cambia de color dependiendo si fue sastifactorio o hubo algun error.
- contiene label y al frente un icon/imagen.
- Navegacion (icono "x")


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| style          | String           | False     ||
| navigation           |CHSDKCongratsFloxNavigation   | False     ||
| title           |CHSDKCongratsFloxLabel   | False     ||
| subtitle           |CHSDKCongratsFloxLabel   | True     ||
| thumbnail           |CHSDKCongratsFloxImage   | True     ||
| badge           |CHSDKCongratsFloxImage   | True     ||

Model:

```json
{
    "ui_type": "banner_congrats",
    "data": {
        "title": {
            "rich": [
            ],
            "accessibility": "Pague os 10000 Real restantes via Boleto para garantir sua compra"
        },
        "navigation": {
            "icon": {
                "type": "icon",
                "data": {
                    "local": "close"
                }
            },
            "event": {
                "type": "go_to_home",
                "data": {}
            }
        },
        "style": "success",
        "thumbnail": {
            "data": {
                "url": "https://http2.mlstatic.com/D_824658-MLB43220259465_082020-O.jpg",
                "modifier": "circle",
                "alt": "Capacete"
            },
            "type": "image"
        },
        "badge": {
            "type": "icon",
            "data": {
                "id": "buflo_congrats_banner_pending_reference"
            }
        }
    }
}
```

Visualizacion:

<img width="378" alt="Captura de Pantalla 2022-03-24 a la(s) 9 26 50 a  m" src="https://user-images.githubusercontent.com/88452146/159938225-4c0d23ff-4674-4e03-8726-89a71e0d6790.png">


## body_congrats_title 
Muestra un Texto. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| text          | CHSDKCongratsFloxLabel           | False     ||

Model:

```json
{
    "ui_type": "body_congrats_title",
    "data": {
        "text": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Ya pagaste R$ 200 con tu tarjeta Santander **** 8480."
                    }
                }
            ]
        },
        "padding": {
            "top": "large",
            "right": "large",
            "left": "large",
            "bottom": "large"
        },
        "modifier": "mid"
    }
}
```

Visualizacion:

<img width="333" alt="Captura de Pantalla 2022-03-24 a la(s) 9 27 47 a  m" src="https://user-images.githubusercontent.com/88452146/159938498-5dd5ee55-cbd9-47d9-a40e-cab231054a37.png">


## body_congrats_description 
Muestra texto para la descripcion. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| text          | CHSDKCongratsFloxLabel           | False     ||

Model:

```json
{
    "ui_type": "body_congrats_description",
    "data": {
        "text": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Para pagar pelo Internet Banking, copie a linha digitável ou ."
                    }
                }
            ]
        }
    }
}
```

Visualizacion:

<img width="346" alt="Captura de Pantalla 2022-03-24 a la(s) 9 29 46 a  m" src="https://user-images.githubusercontent.com/88452146/159938858-e9689916-bb57-45ff-b970-6f42a3d6c261.png">


## information_list_footer 
Muestra un icono y al lado un texto. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| text          | CHSDKCongratsFloxLabel           | False     ||

Model:

```json
{
    "id": "information_list_footer",
    "ui_type": "information_list_footer",
    "data": {
        "text": {
            "rich": [
                {
                    "type": "icon",
                    "value": {
                        "id": "clock"
                    }
                },
                {
                    "type": "text",
                    "value": {
                        "text": "Una vez que pagues, la acreditación demora entre 1 y 2 días hábiles."
                    }
                }
            ]
        }
    }
}
```

Visualizacion:

<img width="345" alt="Captura de Pantalla 2022-03-24 a la(s) 9 37 14 a  m" src="https://user-images.githubusercontent.com/88452146/159940408-60895711-902b-4c3b-a211-3e6752206049.png">



## bar_code 
Muestra una lista de cuotas, con su precio y detalle. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| primary_title          | MLBFFloxComponentLabel           | True     ||
| description           |MLBFFloxComponentLabel   | False     ||
| barcode           |MLBFFloxComponentBase64Image   | False     ||
| modifier           |String   | True     ||

Model:

```json
{
    "id": "bar_code",
    "ui_type": "bar_code",
    "data": {
        "barcode": {
            "src": "iVBORw0KGgoAAAANSUhEUgAAAlgAAAAKAQAAAABAxB2kAAAAW0lEQVR42mP4//+f5IMKiYT0B5KNjW31bRWVDxLb29vnz5OoqEh8+Hye/Pz2Z3JyEnUJCQmS7e1tchIgte3P2+Tk0tt/zm9/2Cbf+BOIZ9T//88wataoWUPELACXinaYKHeyAAAAAABJRU5ErkJggg==",
            "format": "png"
        },
        "description": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "23793.38029 50600.201235 07006.333301 4 87320001000000"
                    }
                }
            ]
        },
        "modifier": "transparent"
    }
}
```

Visualizacion:

<img width="344" alt="Captura de Pantalla 2022-03-24 a la(s) 9 40 10 a  m" src="https://user-images.githubusercontent.com/88452146/159941091-d4f61deb-bb64-4589-a4f8-3136acc2d97d.png">


## progress_loyalty 
Muestra la informacion de MercadoPuntos. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| ring_hexa_color          | String           | True     ||
| ring_percentage           |Float   | True     ||
| ring_number           |Int   | True     ||
| title           |String   | True     ||
| subtitle           |String   | True     ||
| button_title           |String   | True     ||
| button_deep_link           |String   | True     ||

Model:

```json
{
    "ui_type": "progress_loyalty",
    "data": {
        "ring_hexa_color": "#8700FF",
        "ring_number": 5,
        "ring_percentage": 0.43,
        "subtitle": "Assim que o pagamento for aprovado, você ganhará 3,333 pontos por esta compra",
        "title": "Mercado Pontos"
    }
}
```

Visualizacion:

<img width="337" alt="Captura de Pantalla 2022-03-24 a la(s) 9 49 12 a  m" src="https://user-images.githubusercontent.com/88452146/159943134-b2ae1476-6f7c-41b6-9395-76fad88004bf.png">



## discount_loyalty 
Muestra una lista de cuotas, con su precio y detalle. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| discounts_title          | String           | True     ||
| discounts_subtitle           |String   | True     ||
| discounts_button_title           |String   | True     ||
| discounts_fallback_title           |String   | True     ||
| discounts_download_title           |String   | True     ||
| discounts_update_title           |String   | True     ||
| discounts_link           |String   | False     ||
| discounts_fallback_link           |String   | True     ||
| discounts_has_loyalty_ring_section           |Bool   | True     ||
| discounts_items           |[[AnyHashable: Any]]   | True     ||


## payment_option_row 
Tiene lo mismo que [payment_option_row](#payment_option_row) (Se encuentra en el proyecto del SDK)


