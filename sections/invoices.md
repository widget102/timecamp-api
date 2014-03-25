Invoices
======

GET /invoice
----------

Return all invoices.

Example:
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826`

```json
[
  {
    
  }
]
```

POST /invoice
----------

Modify existing invoice

Example:
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826`

Post Variable Array Fields:
* clientId: 1234
* firstName: "Kamil"
* lastName: "Rudnicki"
* organizationName: "Time Solutions Sp. z o.o."
* address: "Kosciuszki 33/4, NIP: 8943003832"
* email: "k.rudnicki2@timecamp.com"

PUT /invoice
----------

Add new invoice.

Example:
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826`

Post Variable Array Fields:
* firstName: "Kamil"
* lastName: "Rudnicki"
* organizationName: "Time Solutions Sp. z o.o."
* address: "Kosciuszki 33/4, NIP: 8943003832"
* email: "k.rudnicki2@timecamp.com"

```json
[
  {

  }
]
```
