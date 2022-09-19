# Reports Detail
This document describes the API endpoint that fetches details about a single report created using report setting.

## Endpoint:
```
    http://digital.kobo.local/api/v1/report-page/<report_id>
    // here report_id is the id for report object obtained from report list api.
```

## Request Method:
`GET`

## Headers:
```{Authorization: Token h1knAjsb891ashbhyva7a}```

The token used here can be obtained from user detail API.

## Response:

```
{
    "id": 91,
    "display_name": "This is test",
    "variable_name": "This_is_test",
    "type": "table",
    "value": "<table border=\"1\" class=\"dataframe\">\n  <thead>\n    <tr style=\"text-align: right;\">\n      <th></th>\n      <th></th>\n      <th></th>\n      <th>Types_of_markets</th>\n      <th>wholesale_market</th>\n      <th>All</th>\n    </tr>\n    <tr>\n      <th>Name_of_agricultural_market</th>\n      <th>Major_services_available</th>\n      <th>Name_of_the_market</th>\n      <th>Haat_Bazaar_open_days</th>\n      <th></th>\n      <th></th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <th>Municipality Market</th>\n      <th>Haat bazar</th>\n      <th>Aarughat market</th>\n      <th>sunday monday tuesday wednesday thursday friday</th>\n      <td>1</td>\n      <td>1</td>\n    </tr>\n    <tr>\n      <th>All</th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <td>1</td>\n      <td>1</td>\n    </tr>\n  </tbody>\n</table>",
    "create_date": "2021-06-30T17:27:34.443247Z",
    "updated_date": null
}
```