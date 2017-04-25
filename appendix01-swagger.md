# Appendix 01 - Swagger

```
{
  "swagger": "2.0",
  "info": {    
    "version": "1.0.0",
    "title": "Flights API",
    "description": "Flights Demo API",
    "termsOfService": "http://swagger.io/terms/",
    "contact": {
      "name": "The Flights Demo Team",
      "email": "demo-flights@redhat.com",
      "url": "http://demo-flights.redhat.com"
    },
    "license": {
      "name": "MIT",
      "url": "http://github.com/3scale/demo-flights/LICENSE-MIT"
    }
  },
  "host": "<yours>",
  "basePath": "/",
  "schemes": [
    "https"
  ],
  "paths": {
    "/flights/intl/flights": {
      "get": {
        "description": "Returns a list of flights",
        "operationId": "Returns a list of flights",
        "parameters": [
          {
            "name": "user_key",
            "in": "query",
            "description": "API/User Key",
            "required": true,
            "type": "string",
            "x-data-threescale-name": "user_keys"
          }
        ],
        "responses": {
          "200": {
            "description": " Flights response",
            "schema": {
              "$ref": "#/definitions/flights"
            }
          },
          "403": {
            "description": "Authentication failed",
            "schema": {
              "$ref": "#/definitions/AuthenticationFailed"
            }
          },
          "default": {
            "description": "unexpected error",
            "schema": {
              "$ref": "#/definitions/Error"
            }
          }
        }
      }
    }
  },
  "definitions": {
    "flights": {
      "type": "object"
    }
  }
}

```



