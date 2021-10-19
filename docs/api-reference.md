# V1

## **Base**
--------------------------------------------
### **GET /**

**RETURNS**
```json
{
    "message": "Ok"
}
```
--------------------------------------------
### **GET /v1/status**

**RETURNS**
```json
{
    "message": "Ok",
    "info": {
        "api": "Ok",
        "database": "Ok"
    }
}
```

## **Products**
--------------------------------------------
### **GET /v1/products**
Returns all products. **Requires ApiKey**

**RETURNS**
```json
{
    "test": {
        "_id": "randomstringhere",
        "name": "test",
        "description": "test",
        "price": 10,
        "attachments": [
            "https://redon.tech"
        ]
    }
}
```
--------------------------------------------
### **POST /v1/create_product**
Create's a product. **Requires ApiKey**

**PARAMETERS**

| Name        | Type   | Description             |
| ----------- | ------ | ----------------------- |
| Name        | String | The product name        |
| Description | String | The product description |
| Price       | Number | The product price       |

**RETURNS**
```json
{
    "info": {
        "name": "test",
        "description": "test",
        "price": 10
    }
}
```
--------------------------------------------
### **POST /v1/update_product**
Update's a product. **Requires ApiKey**

**PARAMETERS**

| Name        | Type   | Description                |
| ----------- | ------ | -------------------------- |
| Oldname     | String | The products original name |
| Newname     | String | The products new name      |
| Description | String | The product description    |
| Price       | Number | The product price          |

**RETURNS**
```json
{
    "info": {
        "name": "test",
        "description": "test",
        "price": 10
    }
}
```
--------------------------------------------
### **DELETE /v1/delete_product**
Delete's a product. **Requires ApiKey**

**PARAMETERS**

| Name | Type   | Description      |
| ---- | ------ | ---------------- |
| Name | String | The product name |

**RETURNS**
```json
{
    "message": "Deleted"
}
```

## **User**
--------------------------------------------
### **GET, POST /v1/user**
Gets a user's information.

**PARAMETERS**

| Name   | Type | Description         |
| ------ | ---- | ------------------- |
| UserId | Int  | The users Roblox Id |

**RETURNS**
```json
{
    "_id": "862543",
    "discordid": "742981374",
    "username": "test",
    "purchases": [
        "test"
    ]
}
```
--------------------------------------------
### **POST /v1/verify_user**
Verify's a user. **Requires ApiKey**

**PARAMETERS**

| Name   | Type | Description         |
| ------ | ---- | ------------------- |
| UserId | Int  | The users Roblox Id |

**RETURNS**
```json
{
    "key": "ADG56"
}
```
--------------------------------------------
### **POST /v1/give_product**
Gives's a user a product. **Requires ApiKey**

**PARAMETERS**

| Name        | Type   | Description         |
| ----------- | ------ | ------------------- |
| UserId      | Int    | The users Roblox Id |
| ProductName | String | The product's name  |

**RETURNS**
```json
{
    "_id": "862543",
    "discordid": "742981374",
    "username": "test",
    "purchases": [
        "test"
    ]
}
```
--------------------------------------------
### **DELETE /v1/revoke_product**
Revoke's a user a product. **Requires ApiKey**

**PARAMETERS**

| Name        | Type   | Description         |
| ----------- | ------ | ------------------- |
| UserId      | Int    | The users Roblox Id |
| ProductName | String | The product's name  |

**RETURNS**
```json
{
    "_id": "862543",
    "discordid": "742981374",
    "username": "test",
    "purchases": []
}
```

## **Other**
--------------------------------------------
### **POST /v1/create_purchase**
Gives's a user a product. **Requires ApiKey**

**PARAMETERS**

| Name   | Type   | Description               |
| ------ | ------ | ------------------------- |
| GameId | Int    | The **expierence** id     |
| Name   | String | The name of the purchase  |
| Price  | Int    | The price of the purchase |

**NOTES**
* Make sure that GameId is the **expierence** which can be found in "Configure this Expierence"'s URL
* DO NOT USE THE PLACE ID FOR GameId IT WILL NOT WORK
* The description of the product will be the Name + the Price

**RETURNS**
```json
{
    "ProductId": "23414123"
}
```