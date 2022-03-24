# Modulo Payment - CHOSDK

En esta seccion mostramos la lista y el detalle de los bricks "ui_type" del modulo Payment del proyecto **CHOSDK** en iOS 🍎.

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
- [cho_payment_default_card](#cho_payment_default_card)
- [cho_payment_credits_card](#cho_payment_credits_card)
- [discount_list_row](#discount_list_row)
- [discount_coupon_list_row](#discount_coupon_list_row)
- [discounts_total](#discounts_total)
- [cho_add_coupon_submit_button](#cho_add_coupon_submit_button)
- [cho_payment_consumer_credits_card](#cho_payment_consumer_credits_card)
- [cho_payment_account_money_default_card](#cho_payment_account_money_default_card)
- [cho_sdk_payment_installment_carousel_item](#cho_sdk_payment_installment_carousel_item)
- [cho_sdk_payment_installments_carousel](#cho_sdk_payment_installments_carousel)

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
