##Get Brands Metadata

* `GET /options/brands` will return brands metadata, that will be used as parameter on others endpoints.

```shell
curl \
-H "username: $SMXUSER" \
-H "token: $TOKEN" \
"http://$INSTANCE.smxecho.com/ws/$INSTANCE/echo/options/brands"
```

```json
[
  {
    "description": "Pepsi",
    "enabled": true,
    "color": "fa5c5c",
    "id": 2,
    "type": "BRAND",
    "display": "Pepsi"
  },
  {
    "description": "Philips",
    "enabled": true,
    "color": "72bbe3",
    "id": 1,
    "type": "BRAND",
    "display": "Philips"
  }
]
```
