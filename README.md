# my_serverless_application
Estudos Dio.me Serverless


Roteiro da aula

->Configurações IAM
	-Criar role
	-Adicionar manualmente actions	
	-Add inline policy
		-Choose service - dynamodb
			-Manual actions
				"dynamodb:getItem",
                		"dynamodb:deleteItem",
                		"dynamodb:scan",
                		"dynamodb:putItem",
                		"dynamodb:updateItem"

->Configurações da API

    -Habilitar CORS no root resource
    -Integrar com lambda proxy -> eventos
    -Method request - put
        Auth IAM
        Request validator - body
        http request header - Content-Type
            -Models
            -Create model
                -Content Type: application/json
        
        Request body  - add model - application/json 

        -Test Method
            -Headers - "Content-Type":"application/json"
            -Request body
------JSON
{
    "id":"item004",
    "itemName": "Item005",
    "itemPrice": 1200
}

    -Method request - List
   - Method request - Delete
        -Request validator - headers
            -http request header - Content-Type
