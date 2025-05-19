# simple-weather-api-docs
Welcome to the **Simple Weather Forcast Api**.
This RESTful API provides current weather data for any city in the world.
- **Base Url:** ``https://api.simpleweather.com/v1``
- **Format:** `JSON`

---
## Authentication
This API uses **API key-based** authentication.

Include your API key as a query parameter in each request:

```bash
?apikey=your_api_key
```
**Example:**

```bash
GET /weather/today?city=Lagos&apikey=abc123
```

---

## End Points
### Get todays weather

```http
GET /weather/today
```

**Query parameters**

| Name   | Type   | Required | Description      |
|--------|--------|----------|------------------|
| city   | string | Yes      | Name of the city |
| apikey | string | Yes      | Your API key     |


## Example Request

```bash
GET https://api.simpleweather.com/v1/weather/today?city=Accra&apikey=abc123
```

---

## Example Response

```json
{
  "city": "Accra",
  "temperature": 29,
  "unit": "Celsius",
  "condition": "Partly Cloudy",
  "humidity": 82,
  "wind_speed": "18 km/h"
}
```

---

## Error Codes

| Code | Message           | Description               |
|------|-------------------|---------------------------|
| 401  | Unauthorized       | Invalid or missing API key |
| 404  | Not Found          | City not found             |
| 429  | Too Many Requests  | Rate limit exceeded        |

---

## Support

For questions or issues, contact:  
**support@simpleweather.com**



