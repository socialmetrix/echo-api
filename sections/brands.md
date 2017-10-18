## Get Brand Reputation

* `GET /echo/reputation/brands` will return brands reputation.

You MUST provide this parameters:

parameter | format | example | description
--- | --- | --- | ---
startDate | YYYY-MM-DD | 2015-01-24 | Starting range
endDate | YYYY-MM-DD | 2015-02-23 | Ending range (including)

Optional parameters are:

parameter | format | example | description
--- | --- | --- | ---
groupingHours | 1 or 24 | 24 | Group results as 24hours period, ie: Days
previousPeriod | Boolean | false | Should include Previously period

Example request:

```shell
curl \
  -H "username: $SMXUSER" \
  -H "token: $TOKEN" \
  "http://$INSTANCE.smxecho.com/ws/$INSTANCE/echo/reputation/brands?startDate=2015-02-01&endDate=2015-02-28"
```

```json
[
  {
    "previous": {
      "startDate": "2015-01-04 00:00",
      "endDate": "2015-01-31 23:59",
      "values": {
        "POSITIVE": 2,
        "NEGATIVE": 10
      }
    },
    "id": 2,
    "type": "BRAND",
    "current": {
      "startDate": "2015-02-01 00:00",
      "endDate": "2015-02-28 23:59",
      "values": {
        "POSITIVE": 2,
        "NEGATIVE": 1
      }
    },
    "parentId": 2,
    "display": "Pepsi"
  }
]
```
