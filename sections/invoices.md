Invoices
======

GET /invoice
----------

Return all invoices.

Example:
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826`

```json
{
    {"8":
      {
        "invoiceId":8,
        "clientId":35,
        "invoiceNumber":"XYZ-05c",
        "description":"",
        "issueDate":"2013-09-16",
        "dueDate":"0000-00-00",
        "editDate":"2013-11-28 13:30:10",
        "status":2,
        "sentDate":"0000-00-00 00:00:00",
        "viewedDate":"0000-00-00 00:00:00",
        "addDate":"2013-09-01 08:00:00",
        "paidDate":"0000-00-00 00:00:00",
        "noteToClient":"Pay asap,dude.",
        "pass":"",
        "poNumber":"",
        "userId":1821,
        "currencyId":2,
        "rootGroupId":1208,
        "publicHash":"91ff5eea64bf001b003d3552119db97b95948aa2",
        "quote":false,
        "entries":
          [
            {
              "invoiceId":8,
              "invoiceEntryId":1,
              "description":"MainPage",
              "type":0,
              "quantity":1,
              "unitCost":1,
              "taxId":2,
              "name":"Design"
            },
            {
              "invoiceId":8,
              "invoiceEntryId":2,
              "description":"asdfasdfasdfasd",
              "type":0,
              "quantity":3,
              "unitCost":14,
              "taxId":11,
              "name":"Programming"
            }
          ]
        }
}
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
