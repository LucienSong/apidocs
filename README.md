# API Documentations for Chaince

## Restful
* The base restful URI: **https://api.chaince.com**
* **JSON** is used as returned data format along with HTTP status code `200`
* **JSON {"error": "xxx"}** will be returned in case of exceptions with status `4XX` `5XX`

## Websocket
* The websocket URI: **wss://api.chaince.com/websocket**

# Endpoints

Name | Description
------------ | ------------ 
[restful-market](./restful-market.md) | currencies and pairs in market 
[restful-quotations](./restful-quotations.md) | tickers and klines
[restful-orders](./restful-orders.md) | submit and cancel orders, active and today orders
[restful-pairs](./restful-pairs.md) | orderbook, trades and ticker
[websocket-trading](./websocket-trading.md) | orders and accounts involved in trading
[websocket-pairs](./websocket-pairs.md) | trades, orderbook change for every trading
[websocket-tickers](./websocket-tickers.md) | ticker and 10 levels orderbook
[authentication](./authentication.md) | payload, signing and authentication

## Root / Ping

```
GET /
```
Root path. can be used as a ping

**Response:**
```json
{
  "api": "chaince",
  "version": "v1"
}
```

**Ratelimit:**
60 requests / 60 seconds
