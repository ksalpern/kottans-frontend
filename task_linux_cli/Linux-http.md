### HTTP:

#### HTTP Is a Hypertext Transfer Protocol 

![](https://cdn.tutsplus.com/cdn-cgi/image/width=466/net/authors/jeremymcpeak/http1-request-response.png)

The HTTP protocol supports a mix of network configurations. The browser is one of the many possible clients which can raise a request. The requests are sent, and responses are received over the TCP/IP layer. The default port for HTTP communication is port 80, but this can be configured differently for different applications.

#### HTTP Requests

Here's a typical HTTP request:

> GET /articles/http-basics HTTP/1.1
Host: www.articles.com
Connection: keep-alive
Cache-Control: no-cache
Pragma: no-cache
Accept: text/html, application/xhtml+xml, application/xml;q=0.9, */*;q=0.8

#### HTTP Request Verbs

There are four universally applicable HTTP verbs in a request:

- GET: fetch a resource from the server. For a GET request, the URL should carry all the required pieces of information for the server to spot the right resource. It does not have a message body.
- POST: create a new resource. The request has an optional payload which helps the server create a new resource.
- PUT: update an existing resource. The request should have an optional payload to help the server update an existing resource.
- DELETE: delete an existing resource.

#### HTTP Responses

The response is similar in structure to a request message, except for the status line and headers.

- status line: includes a status code that indicates whether the request succeeded (status code 200) or why the request failed. It also includes the HTTP version and a very brief description of the status.
-  headers: additional information about the response—for example, the content type or information about the server. 
- body (optional): the content of the response. For example, this might be the HTML content of a requested web page or the binary data of an image.

A successful response from the server will have a status line similar to **HTTP/1.1 200 OK**.

#### Tools to View HTTP Traffic

the Chrome or Webkit inspector

![](https://cms-assets.tutsplus.com/cdn-cgi/image/width=850/uploads/users/2790/posts/39788/image-upload/Screenshot_2022_01_28_at_9_24_03_PM.jpg)

There are also web debugging proxies, like Fiddler and Charles Proxy  or OSX. 

![](https://cms-assets.tutsplus.com/cdn-cgi/image/width=850/uploads/users/2790/posts/39788/image-upload/fiddler_classic_ui_1_.jpg)

#### Receiving an HTTP Request With Express

Express provides a simple API for writing web servers. I won't cover the details of the API. Instead, I'll show you an example of how Express uses HTTP requests and responses.

##### Express Hello World

**const app = express()**
 
**app.get('/', (req, res) => {**
    **res.send('Hello World!')**
**})**
 
**app.get('*', (req, res) => {**
    **res.sendStatus(401);**
**})**
 
**app.listen(3000, () => {**
    **console.log(`Example app listening on port ${port}`)**
**})**


#### Persistent Connections

In a traditional setting, web clients tend to open connections for a specific website. And this site is likely to initiate multiple HTTP requests. For example, one request can be to fetch an inline image, and another request could be to get CSS styles. The likelihood of raising requests in the near future is called site locality. 

The benefits of using persistent connections are:

- avoid delays due to slow setup
- avoid slow start congestion during the adaptation phase
- ensure faster data transfer

#### Basic Authentication

![](https://cdn.tutsplus.com/cdn-cgi/image/width=536/net/authors/jeremymcpeak/http2-authentication.png)

#### Linux survival

##### Some useful commands:

**cd**  changes to another directory

**mkdir**  makes a new directory

**'*'** wildcard represents all files

**rm** removes files

**cp** copy files

**rmdir** removes empty directories

**~** symbol means home directory

**.** symbol means current directory

**df** command shows free disk space

**grep** command finds words in text


Check [HTTP: The Protocol Every Web Developer Must Know—Part 1](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177) and [HTTP: The Protocol Every Web Developer Must Know—Part 2](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-2--net-31155) for more information.


[come back to README](../README.md)