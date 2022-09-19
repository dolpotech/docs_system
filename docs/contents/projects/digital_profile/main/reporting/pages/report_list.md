# Reports List
This document describes the API endpoint that fetches details about all the reports created.
These reports are the reports created from report settings.

## Endpoint:
```http://digital.kobo.local/api/v1/report-page```

## Request Method:
`GET`

## Headers:
```{Authorization: Token h1knAjsb891ashbhyva7a}```

The token used here can be obtained from user detail API.

## Response:

```
[
    {
        "id": 90,
        "display_name": "family info",
        "variable_name": "family_info",
        "type": "table",
        "value": "<table border=\"1\" class=\"dataframe\">\n  <thead>\n    <tr>\n      <th></th>\n      <th>Irrigated_land_hectre</th>\n      <th colspan=\"3\" halign=\"left\">Meat_kg</th>\n      <th>Production_quinton_year</th>\n      <th>Production_sale_quinton_year</th>\n      <th>Quantity1</th>\n      <th>Quantity_D_A_P_kg</th>\n      <th>Quantity_Potas_kg</th>\n      <th colspan=\"3\" halign=\"left\">Total_number_available</th>\n      <th>Ward_Number</th>\n      <th>benefited_number_of_families</th>\n    </tr>\n    <tr>\n      <th></th>\n      <th>mean</th>\n      <th colspan=\"3\" halign=\"left\">mean</th>\n      <th>mean</th>\n      <th>mean</th>\n      <th>mean</th>\n      <th>mean</th>\n      <th>mean</th>\n      <th colspan=\"3\" halign=\"left\">mean</th>\n      <th>mean</th>\n      <th>mean</th>\n    </tr>\n    <tr>\n      <th>In_what_type_of_land_your_anim</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n      <th>Own</th>\n      <th>Rent</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n      <th>Own</th>\n      <th>Rent</th>\n      <th>Governmental</th>\n      <th>Governmental</th>\n    </tr>\n    <tr>\n      <th>For_what_reason_are_you_raisin</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n      <th>Economic_benefit</th>\n    </tr>\n    <tr>\n      <th>Yearly_income_Rs</th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <th></th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <th>10000</th>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>100.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>4.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n    </tr>\n    <tr>\n      <th>20000</th>\n      <td>NaN</td>\n      <td>50005.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>777.5</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n    </tr>\n    <tr>\n      <th>30000</th>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>2000.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>56.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n    </tr>\n    <tr>\n      <th>50000</th>\n      <td>3.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>10.0</td>\n      <td>9.0</td>\n      <td>5.0</td>\n      <td>3.0</td>\n      <td>2.0</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>NaN</td>\n      <td>2.0</td>\n      <td>1.0</td>\n    </tr>\n  </tbody>\n</table>",
        "create_date": "2021-06-27T11:06:33.059982Z",
        "updated_date": null
    },
    {
        "id": 91,
        "display_name": "This is test",
        "variable_name": "This_is_test",
        "type": "table",
        "value": "<table border=\"1\" class=\"dataframe\">\n  <thead>\n    <tr style=\"text-align: right;\">\n      <th></th>\n      <th></th>\n      <th></th>\n      <th>Types_of_markets</th>\n      <th>wholesale_market</th>\n      <th>All</th>\n    </tr>\n    <tr>\n      <th>Name_of_agricultural_market</th>\n      <th>Major_services_available</th>\n      <th>Name_of_the_market</th>\n      <th>Haat_Bazaar_open_days</th>\n      <th></th>\n      <th></th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <th>Municipality Market</th>\n      <th>Haat bazar</th>\n      <th>Aarughat market</th>\n      <th>sunday monday tuesday wednesday thursday friday</th>\n      <td>1</td>\n      <td>1</td>\n    </tr>\n    <tr>\n      <th>All</th>\n      <th></th>\n      <th></th>\n      <th></th>\n      <td>1</td>\n      <td>1</td>\n    </tr>\n  </tbody>\n</table>",
        "create_date": "2021-06-30T17:27:34.443247Z",
        "updated_date": null
    }
]
```