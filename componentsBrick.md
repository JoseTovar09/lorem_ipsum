# Components

En esta seccion mostramos la lista y el detalle de los bricks "ui_type" del proyecto Components en iOS 🍎.

- [button](#button)
- [card](#card)
- [button_container](#button_container)
- [image_label](#image_label)
- [test_app_label](#test_app_label)
- [bar_code](#bar_code)
- [card_information](#card_information)
- [link](#link)
- [detail_row_with_images](#detail_row_with_images)
- [form](#form)
- [input_text](#input_text)
- [submit_button](#submit_button)
- [checkbox](#checkbox)
- [input_spinner](#input_spinner)
- [bulleted_list](#bulleted_list)
- [text_code](#text_code)
- [input_card_radio_button](#input_card_radio_button)
- [input_card_radio_button_group](#input_card_radio_button_group)
- [redirect_separator](#redirect_separator)
- [switch](#switch)
- [card_medium_container](#card_medium_container)


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

<img width="375" alt="Captura de Pantalla 2022-03-05 a la(s) 2 04 54 p  m" src="https://user-images.githubusercontent.com/88452146/156896774-da4e3db1-641b-485a-ad58-985ab3b00869.png">



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

<img width="376" alt="Captura de Pantalla 2022-03-24 a la(s) 9 07 23 a  m" src="https://user-images.githubusercontent.com/88452146/159934274-41c08ef0-3c3d-417d-96ac-7b09b7b89809.png">



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

## test_app_label 
Muestra un texto con fondo gris 

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| text          | String           | False     ||
Model:

```json
{
  "ui_type": "test_app_label",
  "data": {
    "text": "SWITCH SEPARATOR"
  }
}
```

Visualizacion:

<img width="378" alt="Captura de Pantalla 2022-03-24 a la(s) 3 58 44 p  m" src="https://user-images.githubusercontent.com/88452146/160009189-fb705688-1d54-4d0c-9104-8c830d26a324.png">

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

<img width="344" alt="Captura de Pantalla 2022-03-24 a la(s) 9 40 10 a  m" src="https://user-images.githubusercontent.com/88452146/159941091-d4f61deb-bb64-4589-a4f8-3136acc2d97d.png">

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

<img width="346" alt="Captura de Pantalla 2022-03-24 a la(s) 9 20 24 a  m" src="https://user-images.githubusercontent.com/88452146/159936856-4e115675-9b33-4be1-b2c3-6af0f586ed1d.png">


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

<img width="352" alt="Captura de Pantalla 2022-03-05 a la(s) 2 34 10 p  m" src="https://user-images.githubusercontent.com/88452146/156898124-9c7cf886-7489-4ae7-bce1-66c9fd06601a.png">


## submit_button

botón para enviar datos del formulario. Tiene el mismo data que el [button](#button). (Se encuentra en el proyecto de Components)
* tiene el objeto Event que es el que contiene la lógica para enviar los datos del formulario.

Visualización: 

<img width="351" alt="Captura de Pantalla 2022-03-05 a la(s) 3 02 33 p  m" src="https://user-images.githubusercontent.com/88452146/156898427-9481f679-6624-4b05-b94f-aca07bf499aa.png">


## checkbox 
Se encuentra en el proyecto de Componnets. 

Model:

```json
{
  "ui_type": "checkbox",
  "data": {
    "checked": true,
    "text": "Sem número",
    "match_behaviour": "makeFieldOptional",
    "event": {
      "id": "checkbox_update",
      "type": "update_bricks",
      "data": {
        "bricks": [
          {
            "ui_type": "input_text",
            "data": {
              "disabled_text": "SN"
            },
            "id": "street_number"
          }
        ]
      }
    },
    "optional_value": "SN"
  }
}
```

Visualizacion:

<img width="381" alt="Captura de Pantalla 2022-03-24 a la(s) 10 36 04 a  m" src="https://user-images.githubusercontent.com/88452146/159953348-e2e673ba-e721-4f09-a168-81be1c483749.png">


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

<img width="372" alt="Captura de Pantalla 2022-03-05 a la(s) 4 22 19 p  m" src="https://user-images.githubusercontent.com/88452146/156900288-5dc21e23-1901-4640-b944-1ba63cf8849d.png">

## input_card_radio_button_group

Tiene un sctak donde agrupa N [input_card_radio_button](#input_card_radio_button) en una card, No tiene data (Se encuentra en el proyecto de Components)

Visualizacion: 

<img width="379" alt="Captura de Pantalla 2022-03-05 a la(s) 4 51 10 p  m" src="https://user-images.githubusercontent.com/88452146/156901044-2c09f2b1-f5d2-492b-a0fb-4b3eedb35560.png">


## list_container 

Contenedor de lista (Se encuentra en el proyecto de Components).


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title               | {Rich}           | True    |Texto que aparece al lado del radio button.|
| modifier            | String Enum    | True     | separator \| all_separator |
| footer_action       | MLBFFloxComponentLabelFooter    | True     |Footer al final de la lista|


Visualizacion:

<img width="352" alt="Captura de Pantalla 2022-03-05 a la(s) 4 31 14 p  m" src="https://user-images.githubusercontent.com/88452146/156900468-2cb278e2-8605-4de3-9893-16921305309b.png">



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

<img width="100" alt="Captura de Pantalla 2022-03-05 a la(s) 4 39 22 p  m" src="https://user-images.githubusercontent.com/88452146/156900646-c94206b2-acbc-4550-9428-84e2945df7a7.png">


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

<img width="348" alt="Captura de Pantalla 2022-03-05 a la(s) 5 45 51 p  m" src="https://user-images.githubusercontent.com/88452146/156902334-ae7fbff6-d4cd-4da8-8b26-a598455ff7ee.png">


## link_container 
Muestra elementos (label con accion y icon) dependiendo de su orientacion. 

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| orientation          | String           | True     ||

Model:

```json
{
  "id": "link_container",
  "ui_type": "link_container",
  "data": {
    "orientation": "vertical"
  },
  "bricks": []
}
```

Visualizacion:

<img width="370" alt="Captura de Pantalla 2022-03-24 a la(s) 4 11 09 p  m" src="https://user-images.githubusercontent.com/88452146/160010915-04840ce9-a34d-4454-bc90-0400f8697f08.png">

<img width="381" alt="Captura de Pantalla 2022-03-24 a la(s) 4 13 16 p  m" src="https://user-images.githubusercontent.com/88452146/160011192-36e252be-4355-4231-bda1-95a52c9e56f1.png">



## link 
Muestra un label con accion.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| text          | MLBFFloxComponentLabel           | False     ||
| event           |FloxEvent   | False     ||
| modifier           |String   | True     ||

Model:

```json
{
  "ui_type": "link",
  "data": {
    "text": {
      "rich": [
        {
          "type": "icon",
          "value": {
            "id": "phone"
          }
        },
        {
          "type": "text",
          "value": {
            "text": "  Llamar"
          }
        }
      ],
      "accessibility": "Llamar"
    },
    "event": {
      "type": "call_phone",
      "data": {
        "phone_number": "133332221"
      }
    }
  }
}
```

Visualizacion:

<img width="84" alt="Captura de Pantalla 2022-03-24 a la(s) 4 17 58 p  m" src="https://user-images.githubusercontent.com/88452146/160011880-c3b8233c-a902-40a4-8ac1-540ce33520ee.png">


## detail_row_with_images 
Muestra titulo, descripcion y al frente la imagen en forma circular.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| intro          | MLBFFloxComponentLabel           | False     ||
| title           |MLBFFloxComponentLabel   | False     ||
| assets           |CHSDKCongratsFloxLabel   | True     ||

Model:

```json
{
  "ui_type": "detail_row_with_images",
  "data": {
    "intro": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "2 paquetes"
          }
        }
      ]
    },
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Llegan entre el 30 de noviembre y 3 de diciembre"
          }
        }
      ]
    },
    "assets": [
      {
        "type": "image",
        "data": {
          "url": "https://mla-s2-p.mlstatic.com/602023-MLA28139871711_092018-O.jpg",
          "alt": "producto 1"
        }
      },
      {
        "type": "image",
        "data": {
          "url": "https://mla-s2-p.mlstatic.com/667329-MLA28139871712_092018-O.jpg",
          "alt": "producto 2"
        }
      },
      {
        "type": "custom_text",
        "data": {
          "text": "+2"
        }
      }
    ]
  }
}
```

Visualizacion:

<img width="339" alt="Captura de Pantalla 2022-03-24 a la(s) 4 19 28 p  m" src="https://user-images.githubusercontent.com/88452146/160012054-dfae4030-fd7b-4e7b-be5a-3f25e015e5d5.png">



## input_spinner 
Contiene un campo de texto tipo selector.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| name          | String           | False     ||
| label           |String   | True     ||
| options           |String   | False     ||
| value           |String   | True     ||
| event_focus           |FloxEvent   | True     ||

Model:

```json
{
  "ui_type": "input_spinner",
  "data": {
    "name": "input_spinner",
    "label": "Estado",
    "options": [
      "Sao Pablo",
      "Río de Janeiro",
      "River plate"
    ],
    "value": "Río de Janeiro",
    "constraints": {
      "triggered_constraints": [
        {
          "name": "required",
          "value": true,
          "error_message": "REQUIRED"
        }
      ]
    }
  }
}
```

Visualizacion:

<img width="381" alt="Captura de Pantalla 2022-03-24 a la(s) 4 30 06 p  m" src="https://user-images.githubusercontent.com/88452146/160013642-86c4491a-9866-4d15-9976-7dee83eed771.png">


## bulleted_list 
Muestra una lista de texto con viñetas o enumeradas.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| values          | [[AnyHashable: Any]]           | False     ||

Model:

```json
{
    "ui_type": "bulleted_list",
    "data": {
        "values": [
          {
            "bullet": {
              "rich": [
                {
                  "type": "text",
                  "value": {
                    "text": "1.",
                    "modifier": "bold"
                  }
                }
              ]
            },
            "text": {
              "rich": [
                {
                  "type": "text",
                  "value": {
                    "text": "Accesse seu Internet Banking ou app de pagamentos."
                  }
                }
              ]
            }
          },
          {
            "bullet": {
              "rich": [
                {
                  "type": "text",
                  "value": {
                    "text": "2.",
                    "modifier": "bold"
                  }
                }
              ]
            },
            "text": {
              "rich": [
                {
                  "type": "text",
                  "value": {
                    "text": "Elige pagar con Pix."
                  }
                }
              ]
            }
          }
        ]
      }
}
```

Visualizacion:

<img width="335" alt="Captura de Pantalla 2022-03-24 a la(s) 4 34 44 p  m" src="https://user-images.githubusercontent.com/88452146/160014251-289286d8-5dde-4d6a-847f-b514067aa6ab.png">


## text_code 
Componente de texCode con o sin titulo, la cual visualiza en una card el codigo en texto.

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| code          | MLBFFloxComponentLabel           | False     ||
| title           |MLBFFloxComponentLabel   | True     ||

Model:

```json
{
    "id": "code",
    "ui_type": "text_code",
    "data": {
        "code": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "00020101021226720014br.gov.brasdasdasdasdasdsas",
                        "modifier": "bold"
                    }
                }
            ]
        }
    }
}
```

Visualizacion:

<img width="340" alt="Captura de Pantalla 2022-03-24 a la(s) 4 37 25 p  m" src="https://user-images.githubusercontent.com/88452146/160014553-bb762edc-fa87-407f-9df4-3ed1469b13c0.png">


## redirect_separator 
Compoenente que rederigir la app, la cual tiene dos imagenes y en la mitad la animacion del load. contiene label(title y description)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| origin_icon          | MLBFFloxComponentImageModel           | True     ||
| destination_icon           |MLBFFloxComponentImageModel   | True     ||
| title           |MLBFFloxComponentLabel   | False     ||
| subtitle           |MLBFFloxComponentLabel   | False     ||

Model:

```json
{
    "ui_type": "redirect_separator",
    "data": {
        "origin_icon": {
            "accessibility": "PSE",
            "data": {
                "id": "buflo_reference_pse"
            },
            "type": "icon"
        },
        "destination_icon": {
            "accessibility": "Mercado Libre",
            "data": {
                "id": "buflo_reference_meli"
            },
            "type": "icon"
        },
        "title": {
            "rich": [
                {
                    "type": "text",
                    "value": {
                        "text": "Te estamos regresando a Mercado Libre"
                    }
                }
            ]
        },
        "subtitle": {
            "rich": [
            ]
        }
    }
}
```

Visualizacion:

![ezgif com-gif-maker-20](https://user-images.githubusercontent.com/88452146/160015410-105b32c2-fca5-4fee-b9ae-fd422c6e8507.gif)


## card_medium_container 
Contendor que contiene un stackView. es utilizado para agregar componentes [image_label](#image_label)

- No tiene DATA


Model:

```json
 {
  "id": "card_medium_container",
  "ui_type": "card_medium_container",
  "bricks": []
}
```
