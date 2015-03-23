#Socialmetrix Echo API

Below you will find the documentation for [Socialmetrix Echo](http://socialmetrix.com/#products) API.
If you have any doubts or suggestions you can [contact us](mailto:product@socialmetrix.com) directly.

##Getting Started

In order to access our API you need to get your credentials consisting of a username and a token; please refer to your account executive to obtain them. They should look like this: 

```
Username: arjones
Token: e621ef33-62b0-4a44-9c9c-559f40b546cb
```

##API base URL
Our current API uses your **Echo Instance** as **base url**. Your instance is defined at your URL, e.g.: http://socialmetrix-lat.smxecho.com/ , then your instance is `socialmetrix-lat`.

Once you have the instance, you can setup the base url as follows:
`http://$INSTANCE.smxecho.com/ws/$INSTANCE/echo`

##Authentication
Once you have your credentials you MUST include them as part of HTTP HEADER.
As an example, using `curl`:

```shell
INSTANCE=socialmetrix-lat
SMXUSER=arjones
TOKEN=e621ef33-62b0-4a44-9c9c-559f40b546cb

curl \
  -H "username: $SMXUSER" \
  -H "token: $TOKEN" \
  -H 'Content-Type: application/json' \
  "http://$INSTANCE.smxecho.com/ws/$INSTANCE/echo/options/brands"
```

##Rate limiting
During this initial phase, the API isn't rate limited, we want to learn from our customers' consumption patterns to provide an easy way to use the API. Keep in mind that misuse or abuse will result in blocking.

##API ready for usage
Currently available endpoints are:

* [/options/brands](sections/brands-metadata.md): Provides information about the **brands metadata**.
* [/reputation/brands](sections/brands.md): Provides information about the **brand reputation**.
* [/sparkline/brands/mentions](sections/mentions.md): Provides information about the **brand's mentions**.
* [/sparkline/brands/authors](sections/authors.md): Provides information about the **brand's authors**.
* [/sparkline/brands/sources](sections/sources.md): Provides information about the **brand's sources**.


##Help us make it better
Please tell us how we can make the API better. If you have a specific feature request or if you found a bug, please use GitHub issues. Fork these docs and send a pull request with improvements.
