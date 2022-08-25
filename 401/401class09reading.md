[<=== Back](../README.md)

# HTTP

## [High-Level HTTP](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)
*from Dev Community by Daniel Golant*

#### The HTTP Request Lifecycle

Steps in the HTTP Request Lifecycle
1. Local processing - The browser determines where to send a request
2. Resolve an IP - Determine where to send a response? (I didn't quite understand this bit)
3. Establish a TCP connection - (Transmission Control Protocol) A connection between client and server is established
4. Send an HTTP request - request sent, find requested resource, and generate HTTP response
5. Tearing Down and Cleaning Up - Client and server perform a "handshake" which signals the end of the connection, the response is processed by the browser.

## [Do a Simple HTTP Request in Java](https://www.baeldung.com/java-http-request)
*from Baeldung*

#### Performing HTTP Requests in Java
(by using the built-in Java class `HttpUrlConnection`)

**HttpUrlConnection**

> The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the *java.net* package.

**Creating a Request**

Using the `openConnection()` method of the URL class creates an instance of *HttpUrlConnection* - creates a connection object, but doesn't establish a connection yet. 

> The *HttpUrlConnection* class is used for all types of requests by setting the *requestMethod* attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

To create a connection to a given URL using GET:

```
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```

**Adding Request Parameters**

> If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value, param2=value to the OutputStream of the HttpUrlConnection instance. *See Baeldung article for code example*

**Setting Request Headers**

Use `setRequestProperty()`:

`con.setRequestProperty("Content-Type", "application/json");`

To read the value of the header: 

`String contentType = con.getHeaderField("Content-Type");`

**Reading the Response**

> Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.

> To execute the request, we can use the getResponseCode(), connect(), getInputStream() or getOutputStream() methods:

```
int status = con.getResponseCode();
Finally, let's read the response of the request and place it in a content String:

BufferedReader in = new BufferedReader(
  new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    content.append(inputLine);
}
in.close();
```
To close the connection, we can use the disconnect() method:

`con.disconnect();`


There are also classes and methodsto work with Configuring Timeouts, Handling Cookies, Handling Redirects, Reading the Response on Failed Requests, and Building the Full Response. See [Baeldung](https://www.baeldung.com/java-http-request) for code examples