# Modulo Shipping, BillingInfo, OneTap y Split - CHOSDK

En esta seccion mostramos la lista y el detalle de los bricks "ui_type" del modulo Shipping, BillingInfo, OneTap y Split del proyecto CHOSDK en iOS 🍎.



## cho_shipping_option_selected_address_card 
Muestra la informacion del envio del item. contiene titulo, descripcion y un label con accion. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||
| address_line           |MLBFFloxComponentLabel   | False     ||
| change_address           |CHSDKLabelWithEvent   | False     ||

Model:

```json
{
  "ui_type": "cho_shipping_option_selected_address_card",
  "data": {
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Endereço"
          }
        }
      ]
    },
    "address_line": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Rua Dona Brazilia Siqueira Ventura 1231, CEP: 89815657 - Chapecó"
          }
        }
      ]
    },
    "change_address": {
      "event": {
        "type": "go_to_address_hub",
        "data": {
        }
      },
      "text": {
        "rich": [
          {
            "type": "text",
            "value": {
              "modifier": "neutral",
              "text": "Editar ou escolher outro"
            }
          }
        ]
      }
    }
  }
}
```

Visualizacion:

<img width="377" alt="Captura de Pantalla 2022-03-24 a la(s) 10 18 16 a  m" src="https://user-images.githubusercontent.com/88452146/159949595-90183b97-aed1-463d-8eb2-612b53e60cb1.png">



## shipping_options_list_stack 
Muestra una lista de opciones de envio. (Se encuentra en el proyecto del SDK)

- No tiene DATA.


Model:

```json
{
  "ui_type": "shipping_options_list_stack",
  "bricks": []
}
```

Visualizacion:

<img width="374" alt="Captura de Pantalla 2022-03-24 a la(s) 10 20 47 a  m" src="https://user-images.githubusercontent.com/88452146/159950152-599fb1f5-0a42-4068-9447-645805ac2ecb.png">



## shipping_options_list_row 
Muestra la informacion de una opcion de envio, viene dentro de [shipping_options_list_stack](#shipping_options_list_stack) (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| height          | String           | True     ||
| selected           |String   | True     ||

Model:

```json
{
  "ui_type": "shipping_options_list_row",
  "data": {
    "style": "quick_selector",
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Chegará entre os dias 1 e 6 abr. no seu endereço"
          }
        }
      ]
    },
    "event": {
      "type": "select_shipping_option",
      "data": {
      }
    },
    "full_price": {
      "rich": [
      ]
    },
    "selected": "true",
    "price": {
      "rich": [
      ]
    }
  }
}
```

Visualizacion:



## one_tap_billing_info 
Muestra un texto con un icono. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| title          | MLBFFloxComponentLabel           | False     ||
| subtitle           |MLBFFloxComponentLabel   | True     ||
| style           |String   | True     ||

Model:

```json
{
  "ui_type": "one_tap_billing_info",
  "data": {
    "title": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "NF-e em nome de Test Test"
          }
        }
      ]
    },
    "padding": {
      "bottom": "large"
    }
  }
}
```

Visualizacion:

<img width="380" alt="Captura de Pantalla 2022-03-24 a la(s) 10 28 34 a  m" src="https://user-images.githubusercontent.com/88452146/159951813-57d804b6-7837-4d1b-851b-352d5fe71733.png">



## section_title 
Contiene dos labels. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| text          | String           | False     ||
| button           |CHSDKButtonSection   | True     ||

Model:

```json
{
  "ui_type": "section_title",
  "data": {
    "text": {
      "rich": [
        {
          "type": "text",
          "value": {
            "text": "Dados pessoais"
          }
        }
      ]
    }
  }
}
```

Visualizacion:

<img width="382" alt="Captura de Pantalla 2022-03-24 a la(s) 10 31 04 a  m" src="https://user-images.githubusercontent.com/88452146/159952351-5a7bbaf0-8832-427f-8cfa-d2d9dbebdeb1.png">



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

<img width="381" alt="Captura de Pantalla 2022-03-24 a la(s) 10 36 04 a  m" src="https://user-images.githubusercontent.com/88452146/159953348-e2e673ba-e721-4f09-a168-81be1c483749.png">


## skeleton_loading 
Muestra loading cuando se esta llamando a OneTap. (Se encuentra en el proyecto del SDK)

Visualizacion:

<img width="387" alt="Captura de Pantalla 2022-03-24 a la(s) 10 40 22 a  m" src="https://user-images.githubusercontent.com/88452146/159954549-eb036191-126f-4ace-ba47-8197fe5291e8.png">



## split_payment_container 
Es el contenedor principal de Split. Contiene un stackView dentro de un ScrollView. (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| event          | FloxEvent           | True     ||

Model:

```json
{
    "ui_type": "split_payment_container",
    "bricks": []
}    
```


## split_payment_card_medium_container 
Contendor que contiene un stackView y se puede alargar su espacio de constraints. Es utilizado para las cards de opciones de pago (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| modifier          | String           | True     ||


Model:

```json
{
  "ui_type": "split_payment_card_medium_container",
  "id": "split_payment_card_medium_container",
  "data": {
      "modifier": "extended"
  },
  "bricks": [
  ]
}
```


## split_payment_form_container 
Contendor que contiene un stackView y se puede alargar su espacio de constraints. Es utilizado para contener los [form_amount](#form_amount)
 (Se encuentra en el proyecto del SDK)

| Atributo            | Tipo             | Opcional | |
|---------------------|------------------|----------|-|
| modifier          | String           | True     ||

Model:

```json
{
  "ui_type": "split_payment_form_container",
  "id": "split_payment_form_container",
  "data": {
  },
  "bricks": [
  ]
}
```

## split_payment_list_container 
Contiene un stackView, se utiliza para mostrar una lista. (Se encuentra en el proyecto del SDK)

- No tiene data
- 
Model:

```json
{
  "ui_type": "split_payment_list_container",
  "id": "split_payment_list_container",
  "bricks": [
  ]
}
```
