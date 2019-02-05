# Azure Function that Exposes LetsEncrypt Challenge Endpoint

This is a very basis Azure Function, using the v2 Functions framework, and written using JS.

The single function is this app exposes an endpoint that conforms to the [LetsEncryps][le] call back endpoint of `/.well-known/acme-challenge`. If does this by...

1. setting the function's route to `.well-known/acme-challenge` within `function.json`
2. setting the routePrefix to an empty string in `host.json`

The result is that you'll see the following endpoint when run locally:

``` bash
Hosting environment: Production
Content root path: /Users/foo/dev/letsencrypt-challenge-function-app
Now listening on: http://0.0.0.0:7071
Application started. Press Ctrl+C to shut down.

Http Functions:

	example1: [GET,POST] http://localhost:7071/.well-known/acme-cache/

```
