Invoices
======

GET /invoice
----------

Return all invoices.

Example:
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826/format/json`

```json
{
    "8":
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
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826/format/json`

PUT /invoice
----------

Add new invoice.

Example:
`https://www.timecamp.com/third_party/api/invoice/api_token/a36cabi96bba83f826/format/json`

Post Variable Array Fields:
* clientId:145
* invoiceNumber:1234
* currencyId:1 (1=USD)
* status:0 (0=DRAFT, 1=PENDING, 2=PAID)
* description:"asdf" (optional)
* issueDate:2014-03-25 (optional)
* noteToClient:"note" (optional)
* poNumber:1234 (optional)
* dueDate:"2014-03-25" (optional)
* entries[0][description]:asdf (optional)
* entries[0][type]:0 (0=SERVICE, 1=PRODUCT)
* entries[0][quantity]:2
* entries[0][unitCost]:22
* entries[0][taxId]:11
* entries[0][name]:asdf
* quote:false (optional)


```json
{
    "clientId":145,
    "invoiceNumber":"1234",
    "description":"",
    "issueDate":"2014-03-25",
    "dueDate":"",
    "editDate":"2014-03-25 08:58:17",
    "status":0,
    "sentDate":"",
    "viewedDate":"",
    "addDate":"2014-03-25 08:58:17",
    "paidDate":"",
    "noteToClient":"",
    "pass":"",
    "poNumber":"",
    "userId":"640",
    "currencyId":1,
    "rootGroupId":"1208",
    "publicHash":"cc897bb3808fc20cde79918b080cd0f635804a65",
    "quote":false,
    "invoiceId":228,
    "entries":
    [
        {
            "invoiceId":228,
            "description":"asdf",
            "type":0,
            "quantity":2,
            "unitCost":22,
            "taxId":11,
            "name":"asdf",
            "invoiceEntryId":598
        }
    ]
}
```
