Clients
======

GET /client
----------

Return all clients.

Example:
`https://www.timecamp.com/third_party/api/client/api_token/a36cabi96bba83f826`

```json
[
  {
    "firstName":"aaaa",
    "lastName":"bbb",
    "organizationName":"Time Solutions Sp. z o.o.",
    "address":"Ko\u015bciuszki 33\/4",
    "currencyId":1,
    "email":"k.rudnicki@timecamp.com",
    "rootGroupId":"1208",
    "addedBy":"640",
    "added":"2014-03-24 17:00:21",
    "clientId":18855
  }
]
```

POST /client
----------

Modify current client

Example:
`https://www.timecamp.com/third_party/api/client/api_token/a36cabi96bba83f826`

Post Variable Array Fields:
* clientId: 1234
* firstName: "Kamil"
* lastName: "Rudnicki"
* organizationName: "Time Solutions Sp. z o.o."
* address: "Kosciuszki 33/4, NIP: 8943003832"
* email: "k.rudnicki2@timecamp.com"

PUT /client
----------

Add new client.

Example:
`https://www.timecamp.com/third_party/api/client/api_token/a36cabi96bba83f826`

Post Variable Array Fields:
* firstName: "Kamil"
* lastName: "Rudnicki"
* organizationName: "Time Solutions Sp. z o.o."
* address: "Kosciuszki 33/4, NIP: 8943003832"
* email: "k.rudnicki2@timecamp.com"

```json
[
  {
    "firstName":"aaaa",
    "lastName":"bbb",
    "organizationName":"Time Solutions Sp. z o.o.",
    "address":"Ko\u015bciuszki 33\/4",
    "currencyId":1,
    "email":"k.rudnicki@timecamp.com",
    "rootGroupId":"1208",
    "addedBy":"640",
    "added":"2014-03-24 17:00:21",
    "clientId":18855
  }
]
```
