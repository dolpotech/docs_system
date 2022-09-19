#koboform Api
[API Official Docs](https://github.com/kobotoolbox/docs/blob/master/source/api.md)

[Community Api Example Link](https://community.kobotoolbox.org/t/kobo-api-examples-using-new-kpi-endpoints/2742)

##Automate Sharing  koboforms (API)
This document describes about API endpoints for sharing koboforms to a user

### Endpoint
```http://kf.qbitsx.com/api/v2/assets/a6KsgAxLV5M3SNsrV3M78D/permission-assignments/```

Note: ``FORMUUID=a6KsgAxLV5M3SNsrV3M78D``

### Request Method
`POST`

### Headers
```{Authorization: Token b11b6d323bf821eee8b4ec3a9089d8afa27f88b7}```

Note: `user token = b11b6d323bf821eee8b4ec3a9089d8afa27f88b7`
The token used here can be obtained from user detail API.

### Body

    `user`: 'http://kf.qbitsx.com/api/v2/users/ward1-data_collector/',
    'permission': 'http://kf.qbitsx.com/api/v2/permissions/add_submissions/',
    `content`: <string: content of report> (nullable)
    `skeleton`: <string: skeleton of report> (nullable)
    
Note:permission add_submissions is a code_name
        code_name could be 

        i. add_submissions
        ii. change_asset
        iii. change_submissions
        iv. validate_submissions
        v. view_asset
        vi. view_submissions

###Python code 
```
req = requests.post('http://kf.qbitsx.com/api/v2/assets/a6KsgAxLV5M3SNsrV3M78D/permission-assignments/',
data={
'user': 'http://kf.qbitsx.com/api/v2/users/ward%s-data_collector/' % number,
'permission': 'http://kf.qbitsx.com/api/v2/permissions/add_submissions/',
}, headers={'Authorization': 'Token b11b6d323bf821eee8b4ec3a9089d8afa27f88b7'}) # token of user narpa_admin1
```
