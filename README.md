## API Documentation

### Base URL localhost:8080

```
@baseUrl = http://localhost:8080
@prettyName = {{event.response.body.prettyName}}
@userId = {{subscription.response.body.subscriber}}
```

### Endpoints

#### POST /events

```
POST {{baseUrl}}/events
Content-Type: application/json

{
  "title": "Ruby Summit",
  "location": "Santa Catarina, Brazil",
  "price": 299.99,
  "startDate": "2023-11-15",
  "endDate": "2023-11-17",
  "startTime": "09:00:00",
  "endTime": "17:00:00"
}
```

#### GET /events

```
GET {{baseUrl}}/events
Content-Type: application/json
```

#### GET /events/:prettyName

```
GET {{baseUrl}}/events/{{prettyName}}
Content-Type: application/json
```

#### GET /subscriptions

```
GET {{baseUrl}}/subscriptions
Content-Type: application/json
```

#### POST /subscriptions/:prettyName

```
POST {{baseUrl}}/subscriptions/{{prettyName}}
Content-Type: application/json

{
  "name": "Mohamed Toreno",
  "email": "mohamed.toreno@gta.com"
}
```

#### POST /subscriptions/:prettyName/:userId

```
POST {{baseUrl}}/subscriptions/{{prettyName}}/{{userId}}
Content-Type: application/json

{
  "name": "Caio Toreno",
  "email": "caio.toreno@gta.com"
}
```

#### GET /subscriptions/:prettyName/ranking

```
GET {{baseUrl}}/subscriptions/{{prettyName}}/ranking
Content-Type: application/json
```

#### GET /subscriptions/:prettyName/ranking/:subscriberId

```
GET {{baseUrl}}/subscriptions/{{prettyName}}/ranking/{{userId}}
Content-Type: application/json
```

#### POST /subscriptions/any-inexistent-event

```
POST {{baseUrl}}/subscriptions/any-inexistent-event
Content-Type: application/json

{
  "name": "Felipe Nascimento",
  "email": "felipe@email.com"
}
```
