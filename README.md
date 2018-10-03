In this example, we show how a JWT filter can be used with the Envoy
proxy.

This repo has been copied and modified from the official lua example as dound(https://www.envoyproxy.io/docs/envoy/latest/configuration/http_filters/lua_filter).

# Usage
1. `docker-compose build`
2. `docker-compose up`
3. `curl -v localhost:8003`

## Sample Output:

401 for any path except /health, which should return a 200 echoing the request