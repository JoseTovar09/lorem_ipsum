# Components

En esta seccion mostramos la lista y el detalle de los bricks "ui_type" del proyecto Components en iOS 🍎.

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
