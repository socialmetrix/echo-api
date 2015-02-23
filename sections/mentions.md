##Get Mentions Time Series

* `GET /sparkline/brands/mentions` provides SUM of MENTIONS grouped by day.

You MUST provide this parameters:

parameter | format | example | description
--- | --- | --- | --- 
startDate | YYYY-MM-DD | 2015-01-24 | Starting range
endDate | YYYY-MM-DD | 2015-02-23 | Ending range (including) 

Optional parameters are:

parameter | format | example | description
--- | --- | --- | --- 
entities | IDs separated by comma | 1,2,4 | Ids from [/options/brands](sections/brands-metadata.md)
opinions | IDs separated by comma | 1,2,3 | Ids from [Opinions table](sections/opinions.md)
groupingHours | 1 or 24 | 24 | Group results as 24hours period, ie: Days
previousPeriod | Boolean | false | Should include Previously period


####IMPORTANT: If you need to report a single brand's mentions, you need to pass the `entities` parameter, otherwise you'll obtain the SUM of all brands activities.

```shell
curl \
-H "username: $SMXUSER" \
-H "token: $TOKEN" \
"http://$INSTANCE.smxecho.com/ws/$INSTANCE/echo/sparkline/brands/mentions?startDate=2015-02-01&endDate=2015-02-05"
```

```json
{
  "current": {
    "opc": 1,
    "values": [
      {
        "startDate": "2015-02-01 00:00",
        "endDate": "2015-02-01 23:59",
        "value": 0
      },
      {
        "startDate": "2015-02-02 00:00",
        "endDate": "2015-02-02 23:59",
        "value": 7
      },
      {
        "startDate": "2015-02-03 00:00",
        "endDate": "2015-02-03 23:59",
        "value": 5
      },
      {
        "startDate": "2015-02-04 00:00",
        "endDate": "2015-02-04 23:59",
        "value": 3
      },
      {
        "startDate": "2015-02-05 00:00",
        "endDate": "2015-02-05 23:59",
        "value": 3
      }
    ]
  }
}
```