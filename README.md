
﻿
# Desafio Java Backend (Aplicação para divisão de conta)

1) Versão do Java: 17

2) Instalar o XAMP, pois, o banco de dados é mysql, criar database com o nome splitbill.

3) Curl para importar no postman (POST - Create Bill):
```bash
curl --location 'http://localhost:8080/bill/save' \
--header 'Content-Type: application/json' \
--data '{
    "discount":"10",
    "addFee":"15",
    "serviceTax":"20",
    "bank":"NUBANK",
    "customer": "55447788",
    "friends":[
        {
            "name":"Andre",
            "phone":"+5511947858112",
            "items":[
                {
                    "itemName":"Bolacha",
                    "price":10
                },
                {
                    "itemName":"Cafe",
                    "price":22
                }
            ]
        },
        {
            "name":"Paulo",
            "phone":"+5511947858112",
            "items":[
                {
                    "itemName":"Bolacha",
                    "price":10
                },
                {
                    "itemName":"Suco",
                    "price":13
                }                
            ]
        }
    ]
}'
```


3) Curl para importar no postman (GET - Lista de Bills):
```bash
curl --location 'http://localhost:8080/bill/all'
```
