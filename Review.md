# Modulo Review - CHOSDK

En esta seccion mostramos la lista y el detalle de los bricks "ui_type" del modulo Review del proyecto **CHOSDK** en iOS 🍎.

- [review_container](#review_container)
- [review_summary_container](#review_summary_container)
- [review_summary_row_title](#review_summary_row_title)
- [review_summary_row_detail](#review_summary_row_detail)
- [review_summary_detail_label](#review_summary_detail_label)
- [review_detail_container](#review_detail_container)
- [review_detail_payment](#review_detail_payment)
- [review_detail_item](#review_detail_item)
- [review_detail_shipping](#review_detail_shipping)


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
