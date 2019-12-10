# Exceptions

## FailedActionException
This exception is thrown when the server returns `400`.

*Solution: Check the response body.*

## NotFoundException
This exception is thrown when the server returns `404`.

*Solution: Check if the resource exists.*

## TimeoutException
This exception is thrown when the request is timeout.

*Solution: Check the connection between your server and panel.*

## ValidationException
This exception is thrown when the server returns `422`, the given data failed to pass validation.

*Solution: Check the data you given.*