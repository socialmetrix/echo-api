#Socialmetrix Echo API

Below you will the documentation for [Socialmetrix Echo](http://socialmetrix.com/#products) API.
Any doubt or suggestion you can [contact us](mailto:product@socialmetrix.com) directly.

##Getting Started

In order to access our API you need to get your credentials consisting of an username and a token, please refer to your account executive to obtain them. They will be like this: 

```
Username: arjones
Token: e621ef33-62b0-4a44-9c9c-559f40b546cb
```

Also, you need to provide a valid Echo Instance, your instance is defined at your URL, for example, if your url is: http://socialmetrix-lat.smxecho.com/ your instance is `socialmetrix-lat`.

##Authentication
Once you have your credentials you MUST include them as part of HTTP HEADER.
As an example, using `curl`:

```shell
INSTANCE=socialmetrix-lat
SMXUSER=arjones
TOKEN=4a78d0f3-XXXX-XXXX-XXXX-142XXXXc37a6

curl \
  -H "username: $SMXUSER" \
  -H "token: $TOKEN" \
  -H 'Content-Type: application/json' \
  "http://$INSTANCE.smxecho.com/ws/$INSTANCE/echo/reputation/brands"
```

##Rate limiting
During this initial phase, the API isn't rate limited, we want to learn from our customers' consumption patterns to provide an easy to use API. Keep in mind that misuse or abuse will be blocked.

##API ready for use
* [/brands](sections/brands.md): Provides information related to Brand Balance.


##Help us make it better
Please tell us how we can make the API better. If you have a specific feature request or if you found a bug, please use GitHub issues. Fork these docs and send a pull request with improvements.
