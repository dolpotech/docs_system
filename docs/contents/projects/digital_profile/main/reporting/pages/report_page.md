# Report(Combined Report of all reports)

This document describes about API endpoints for CRUD operations of Report preparation.
This report defines the single integrated report that contains all the reports, maps and variables.

## Create Endpoint
### Endpoint
```http://digital.kobo.local/api/v1/report```

### Request Method
`POST`

### Headers
```{Authorization: Token h1knAjsb891ashbhyva7a}```

The token used here can be obtained from user detail API.

### Body

    `user`: <integer: id of user>,
    `title`: <string: title of report>,
    `content`: <string: content of report> (nullable)
    `skeleton`: <string: skeleton of report> (nullable)

## List endpoint
### Endpoint
```http://digital.kobo.local/api/v1/report```

### Request Method
`GET`

### Headers
```{Authorization: Token h1knAjsb891ashbhyva7a}```

The token used here can be obtained from user detail API.

### Response
```
    [
        {
            "id": 1,
            "title": "Municipality Report",
            "content": "",
            "skeleton": "",
            "user": 1,
        },
        {
            "id": 2,
            "title": "Municipality Report 2",
            "content": "",
            "user": 1,
            "skeleton": "",
        }
    ]
```

## Detail endpoint
### Endpoint
```http://digital.kobo.local/api/v1/report/<report_id>```

### Request Method
`GET`

### Headers
```{Authorization: Token h1knAjsb891ashbhyva7a}```

The token used here can be obtained from user detail API.

### Response
Example:
`http://digital.kobo.local/api/v1/report/1`

```
    {
        "id": 1,
        "title": "Municipality Report",
        "content": "",
        "user": 1, # id of user,
        "skeleton": ""
    }
```

## Update endpoint
### Endpoint
```http://digital.kobo.local/api/v1/report/<report_id>```

### Request Method
`PUT`

### Headers
```{Authorization: Token h1knAjsb891ashbhyva7a}```

The token used here can be obtained from user detail API.

### Body
    `title`: <string> (required)
    `user`: <id of user> (required)
    `content`: <content of report in string> (nullable)
    `skeleton`: <skeleton in string> (nullable)
