# V1

## Base

### GET /
| Returns |
| ------- |
```
{
    "message": "Ok"
}
```

### GET /v1/status
| Returns |
| ------- |
```
{
    "message": "Ok",
    "info": {
        "api": "Ok",
        "database": "Ok"
    }
}
```

## Products

### POST /v1/create_product
Creates a product. **Requires ApiKey**
| Parameters  |        |                         |
| ----------- | ------ | ----------------------- |
| Name        | String | The product name        |
| Description | String | The product description |
| Price       | Number | The product price       |

| Returns |
| ------- |
```
```