# Organizations

Basic information about your organization

# Available API's


## Get organization

* `GET /organizations/me.json` will return your organization

```json
{
  "id": 1,
  "name": "Your Church",
  "currency": "usd",
  "street": "4600 E. 2nd Street",
  "city": "Edmond",
  "state": "OK",
  "postal_code": "73034",
  "country": "USA",
  "phone": "406-680-5433",
  "created_at": "2012-01-25T00:13:47Z",
  "updated_at": "2013-05-06T03:24:05Z"
}
```

## Get weekly_totals

* `GET /organizations/weekly_totals.json`
* Required parameters: ```category_id```
* Optional parameters: ```week_reference``` (defaults to current week)

```json
{
  "church": {
    "id": 1,
    "name": "Your Church",
    "currency": "usd",
    "street": "4600 E. 2nd Street",
    "city": "Edmond",
    "state": "OK",
    "postal_code": "73034",
    "country": "USA",
    "phone": "406-680-5433",
    "created_at": "2012-01-25T00:13:47Z",
    "updated_at": "2013-05-06T03:24:05Z"
  },
  "category": {
    "id": 1,
    "name": "Attendance",
    "format": "number",
    "created_at": "2012-01-25T00:48:01Z",
    "updated_at": "2012-01-25T00:48:01Z"
  },
  "services_reporting": "103/144",
  "this_week": {
    "reported": "1,758",
    "total": "2,141"
  },
  "last_week": {
    "reported": "1,608",
    "total": "1,975"
  },
  "last_year": {
    "reported": "1,911",
    "total": "2,216"
  }
}
```

## Edit church

* `PUT /organizations/me.json` will update your organization

```json
{
  "name": "Your Church",
  "currency": "usd",
  "street": "4600 E. 2nd Street",
  "city": "Edmond",
  "state": "OK",
  "postal_code": "73034",
  "country": "USA",
  "phone": "406-680-5433",
}
```

This will return ```200 OK``` if the update was a success, along with the current JSON representation of the organization in the response body.
