![boom Logo](https://raw.github.com/hapijs/boom/master/images/boom.png)

HTTP-friendly error objects

[![Build Status](https://secure.travis-ci.org/hapijs/boom.png)](http://travis-ci.org/hapijs/boom)

Lead Maintainer: [Adam Bretz](https://github.com/arb)

#List of friendly errors available

## 4xx Errors

###Boom.badRequest
example payload for `Boom.badRequest('your message');`
```json
{
    "statusCode": 400,
    "error": "Bad Request",
    "message": "your message"
}
```

###Boom.unauthorized
example payload for `Boom.unauthorized('your message');`
```json
{
    "statusCode": 401,
    "error": "Unauthorized",
    "message": "your message"
}
```

###Boom.forbidden
example payload for `Boom.forbidden('your message');`
```json
{
    "statusCode": 403,
    "error": "Forbidden",
    "message": "your message"
}
```

###Boom.notFound
example payload for `Boom.notFound('your message');`
```json
{
    "statusCode": 404,
    "error": "Not Found",
    "message": "your message"
}
```

###Boom.methodNotAllowed
example payload for `Boom.methodNotAllowed('your message');`
```json
{
    "statusCode": 405,
    "error": "Method Not Allowed",
    "message": "your message"
}
```

###Boom.notAcceptable
example payload for `Boom.notAcceptable('your message');`
```json
{
    "statusCode": 406,
    "error": "Not Acceptable",
    "message": "your message"
}
```

###Boom.proxyAuthRequired
example payload for `Boom.proxyAuthRequired('your message');`
```json
{
    "statusCode": 407,
    "error": "Proxy Authentication Required",
    "message": "your message"
}
```

###Boom.clientTimeout
example payload for `Boom.clientTimeout('your message');`
```json
{
    "statusCode": 408,
    "error": "Request Time-out",
    "message": "your message"
}
```

###Boom.conflict
example payload for `Boom.conflict('your message');`
```json
{
    "statusCode": 409,
    "error": "Conflict",
    "message": "your message"
}
```

###Boom.resourceGone
example payload for `Boom.resourceGone('your message');`
```json
{
    "statusCode": 410,
    "error": "Gone",
    "message": "your message"
}
```

###Boom.lengthRequired
example payload for `Boom.lengthRequired('your message');`
```json
{
    "statusCode": 411,
    "error": "Length Required",
    "message": "your message"
}
```

###Boom.preconditionFailed
example payload for `Boom.preconditionFailed('your message');`
```json
{
    "statusCode": 412,
    "error": "Precondition Failed",
    "message": "your message"
}
```

###Boom.entityTooLarge
example payload for `Boom.entityTooLarge('your message');`
```json
{
    "statusCode": 413,
    "error": "Request Entity Too Large",
    "message": "your message"
}
```

###Boom.uriTooLong
example payload for `Boom.uriTooLong('your message');`
```json
{
    "statusCode": 414,
    "error": "Request-URI Too Large",
    "message": "your message"
}
```

###Boom.unsupportedMediaType
example payload for `Boom.unsupportedMediaType('your message');`
```json
{
    "statusCode": 415,
    "error": "Unsupported Media Type",
    "message": "your message"
}
```

###Boom.rangeNotSatisfiable
example payload for `Boom.rangeNotSatisfiable('your message');`
```json
{
    "statusCode": 416,
    "error": "Requested Range Not Satisfiable",
    "message": "your message"
}
```

###Boom.expectationFailed
example payload for `Boom.expectationFailed('your message');`
```json
{
    "statusCode": 417,
    "error": "Expectation Failed",
    "message": "your message"
}
```

###Boom.badData
example payload for `Boom.badData('your message');`
```json
{
    "statusCode": 422,
    "error": "Unprocessable Entity",
    "message": "your message"
}
```

## 5xx Errors

All 5xx errors hide your message from the end user. Your message is recorded in the server log.

###Boom.notImplemented
example payload for `Boom.notImplemented('your message');`
```json
{
    "statusCode": 501,
    "error": "Not Implemented",
    "message": "An internal server error occurred"
}
```

###Boom.badGateway
example payload for `Boom.badGateway('your message');`
```json
{
    "statusCode": 502,
    "error": "Bad Gateway",
    "message": "An internal server error occurred"
}
```

###Boom.serverTimeout
example payload for `Boom.serverTimeout('your message');`
```json
{
    "statusCode": 503,
    "error": "Service Unavailable",
    "message": "An internal server error occurred"
}
```

###Boom.gatewayTimeout
example payload for `Boom.gatewayTimeout('your message');`
```json
{
    "statusCode": 504,
    "error": "Gateway Time-out",
    "message": "An internal server error occurred"
}
```

###Boom.badImplementation
example payload for `Boom.badImplementation('your message');`
```json
{
    "statusCode": 500,
    "error": "Internal Server Error",
    "message": "An internal server error occurred"
}
```

## Helper Methods

###Boom.wrap
example usages of `Boom.wrap(error, statusCode, message);`
```js
var error = Boom.badRequest();
Boom.wrap(error);

// Or

var error = new Error('an error occurred');
Boom.wrap(error);

// Or

var error = new Error();
Boom.wrap(error, 400, 'an error occurred');
```
