# HTTP Requests & Responses
## Request Line
`GET /home.html HTTP/1.1 ` <br/>
`GET` is the HTTP method, `/home.html` is the resource requested and `HTTP 1.1` is the protocol used

## HTTP Methods
HTTP methods indicate the action that the client wishes to perform
| HTTPS Method  | Description |
| ------------- | ------------- |
| GET | Retrieve: Requests a resource on the web server|
| POST | Send: Submits data to a resource on the web server|
| PUT | Update: Replaces a resource on the web server|
| DELETE | Remove: Deletes a resource on the web server|

## HTTP Request Headers
```
Host: example.com
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: */*
Accept-Language: en
Content-type: text/json
```
- The `Host` header specifies the host of the server and indicates where the resource is requested from.
- The `User-Agent` header informs the web server of the application that is making the request (e.g. Windows, Mac, Linux), version, application vendor.
- The `Accept` header informs the web server what type of content the client will accept as the response.
- The `Accept-Language`header indicates the language and optionally the locale that the client prefers.
- The `Content-type` header indicates the type of content being transmitted in the request body.

## HTTP Request Body
HTTP requests can optionally include a request body, often when using the HTTP POST and PUT methods.
```
POST /users HTTP/1.1
Host: example.com
{
 "key1":"value1",
 "key2":"value2",
 "array1":["value3","value4"]
}
```
```
PUT /users/1 HTTP/1.1
Host: example.com
Content-type: text/json
{"key1":"value1"}
```
## HTTP Responses
When the web server is finished processing the HTTP request, it will send back an **HTTP response**.<br/>
`HTTP/1.1 200 OK` <br/>
`HTTP/1.1` is a HTTP protocol version, `200` is the status code and `OK` is a reason phrase, a textual representation of the status code.
## HTTP Response Header
```
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html
```
- The Date header specifies the date and time the HTTP response was generated.
- The Server header describes the web server software used to generate the response.
- The Content-Length header describes the length of the response.
- The Content-Type header describes the media type of the resource returned (e.g. HTML document, image, video).

## HTTP Response Body
Main content of the HTTP response, that may contain images, video, HTML documents, and other media types
```
HTTP/1.1 200 OK
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html

<html>
  <head><title>Test</title></head>
  <body>Test HTML page.</body>
</html>
```
