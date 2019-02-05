# Azure Function that Exposes LetsEncrypt Challenge Endpoint

This is a very basis Azure Function, using the v2 Functions framework, and written using JS.

The single function is this app exposes an endpoint that conforms to the [LetsEncryps][le] call back endpoint of `/.well-known/acme-challenge`. If does this by...

1. setting the function's route to `.well-known/acme-challenge` within `function.json`
2. setting the routePrefix to an empty string in `host.json`
