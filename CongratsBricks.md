# Modulo Congrats - CHOSDK

En esta seccion mostramos la lista y el detalle de los bricks "ui_type" del modulo Congrats del proyecto CHOSDK en iOS 🍎.

- [main](#main)
- [body_congrats](#body_congrats)
- [card](#card)
- [card_information](#card_information)
- [banner_congrats](#banner_congrats)
- [body_congrats_title](#body_congrats_title)
- [body_congrats_description](#body_congrats_description)
- [information_list_footer](#information_list_footer)
- [bar_code](#bar_code)
- [progress_loyalty](#progress_loyalty)
- [discount_loyalty](#discount_loyalty)
- [text_code](#text_code)
- [card_disclaimer](#card_disclaimer)
- [bulleted_list](#bulleted_list)
- [button](#button)
- [button_container](#button_container)
- [payment_option_row](#payment_option_row)
- [message](#message)


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


## text_code 
Se encuentra en el proyecto de [Componets](ComponentsBricks.md). 

## card_disclaimer 
Se encuentra en el proyecto de [Componets](ComponentsBricks.md). 

## bulleted_list 
Se encuentra en el proyecto de [Componets](ComponentsBricks.md). 

## button 
Se encuentra en el proyecto de [Componets](ComponentsBricks.md). 

## button_container 
Se encuentra en el proyecto de [Componets](ComponentsBricks.md). 

## payment_option_row 
Se encuentra en el Modulo de [Payments](PaymentsBricks.md). 


## message 
Muestra card con un titulo, descripcion y icono. (Se encuentra en el proyecto del SDK)


| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | String           | True     ||
| is_dismissible           |Bool   | True     ||
| message           |CHSDKCongratsFloxLabel   | True     ||

Model:

```json
{
  "ui_type": "message",
  "data": {
    "type": "neutral",
    "title":"Titulo.",
    "is_dismissible":false,
    "padding": {
        "top": "large",
        "bottom": "large",
        "left": "large",
        "right": "large"
    },
    "message": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Para recibir factura A cargá los documentos de la empresa en tu próxima compra."
          }
        }
      ]
    }
  }
}
```

Visualizacion:

<img width="340" alt="Captura de Pantalla 2022-03-24 a la(s) 10 06 33 a  m" src="https://user-images.githubusercontent.com/88452146/159947083-5aac114e-59a8-4725-be65-a1bda159d17e.png">
