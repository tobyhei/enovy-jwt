In this example, we show how a JWT filter can be used with the Envoy proxy.

See https://www.envoyproxy.io/docs/envoy/latest/configuration/http_filters/jwt_authn_filter for official docs.

# Usage
1. `docker-compose build`
2. `docker-compose up`
3. Post to any endpoint except /health, e.g `localhost:8000/service` using the following good token as found in https://github.com/envoyproxy/envoy/blob/c7b290085582a089afea078ca17b8ab7709ec51b/test/extensions/filters/http/jwt_authn/test_common.h
 
```
eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJodHRwczovL2V4YW1wbGUuY29tIiwic3ViIjoidGVzdEBleGFtcGxlLmNvbSIsImV4cCI6MjAwMTAwMTAwMSwiYXVkIjoiZXhhbXBsZV9zZXJ2aWNlIn0.cuui_Syud76B0tqvjESE8IZbX7vzG6xA-MDaof1qEFNIoCFT_YQPkseLSUSR2Od3TJcNKk-dKjvUEL1JW3kGnyC1dBx4f3-XxroyL23UbR2eS8TuxO9ZcNCGkjfvH5O4mDb6cVkFHRDEolGhA7XwNiuVgkGJ5Wkrvshih6nqKXcPNaRx9lOaRWg2PkE6ySNoyju7rNfunXYtVxPuUIkl0KMq3WXWRb_cb8a_ZEprqSZUzi_ZzzYzqBNVhIJujcNWij7JRra2sXXiSAfKjtxHQoxrX8n4V1ySWJ3_1TH_cJcdfS_RKP7YgXRWC0L16PNF5K7iqRqmjKALNe83ZFnFIw
```

## Sample Output:

It crashes :(