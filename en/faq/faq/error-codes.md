---
icon: circle-xmark
---

# Common Error Codes

* 4xx (Client Error Status Codes): Generally indicate request syntax errors, authentication failures, or authorization failures that prevent completion of the request.
* 5xx (Server Error Status Codes): Generally indicate server-side errors, server downtime, request processing timeout, etc.

| Error Code | Possible Causes | Solution |
| --- | --- | --- |
| 400 | Request syntax error, cannot be understood by the server. May be caused by incorrect parameter passing, wrong format, etc. | Check and correct request parameters |
| 401 | Unauthorized access, usually authentication or authorization failure | Check if login credentials are correct |
| 403 | Server understands the request but refuses to execute, may be due to insufficient permissions | Check if user permissions are configured correctly |
| 404 | Requested resource does not exist | Check if the request path is correct |
| 429 | Unverified users: Limited to 100 requests per day. If daily requests exceed 100, you will receive a 429 error. | Try to complete identity verification with the model service provider |
| 500 | Internal server error, usually a code bug or service downtime | Check server logs, fix code issues |
| 502 | Server acting as gateway or proxy received an invalid response from upstream server | Check if upstream service is running correctly |
| 503 | Server temporarily unable to process requests, may be overloaded or under maintenance | Scale up server resources or wait for service recovery |
