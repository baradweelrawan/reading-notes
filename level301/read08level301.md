# this is read08 from 301
# APIs / RESTful web API design :
![img](https://hackernoon.com/hn-images/1*lAR9Uh_gJ7dp23e0vhy5Hg.png)

Most modern web applications expose APIs that clients can use to interact with the application. A well-designed web API should aim to support:
  1. Platform independence.
  2. Service evolution.

# What is REST?
A primary advantage of REST over HTTP is that it uses open standards, and does not bind the implementation of the API or the client applications to any specific implementation. For example, a REST web service could be written in ASP.NET, and client applications can use any language or toolset that can generate HTTP requests and parse HTTP responses. There are some of the main design principles of RESTful APIs using HTTP:
   1. REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.
   2. A resource has an identifier, which is a URI that uniquely identifies that resource.
   3. Clients interact with a service by exchanging representations of resources. Many web APIs use JSON as the exchange format.
   4. REST APIs use a uniform interface, which helps to decouple the client and service implementations. For REST APIs built on HTTP, the uniform interface includes using standard HTTP verbs to perform operations on resources. The most common operations are GET, POST, PUT, PATCH, and DELETE.
   5. REST APIs use a stateless request model. HTTP requests should be independent and may occur in any order, so keeping transient state information between requests is not feasible. The only place where information is stored is in the resources themselves, and each request should be an atomic operation.
   6. REST APIs are driven by hypermedia links that are contained in the representation. 

# The maturity model for web APIs:
   1. Level 0: Define one URI, and all operations are POST requests to this URI.
   2. Level 1: Create separate URIs for individual resources.
   3. Level 2: Use HTTP methods to define operations on resources.
   4. Level 3: Use hypermedia,corresponds to a truly RESTful API according to Fielding's definition. In practice, many published web APIs fall somewhere around level 2.

# Organize the API design around resources :
Focus on the business entities that the web API exposes.Creating an order can be achieved by sending an HTTP POST request that contains the order information. The HTTP response indicates whether the order was placed successfully or not. When possible, resource URIs should be based on nouns the resource and not verbs (the operations on the resource.A resource doesn't have to be based on a single physical data item. For example, an order resource might be implemented internally as several tables in a relational database, but presented to the client as a single entity. Avoid creating APIs that simply mirror the internal structure of a database. The purpose of REST is to model entities and the operations that an application can perform on those entities. A client should not be exposed to the internal implementation.Entities are often grouped together into collections (orders, customers). A collection is a separate resource from the item within the collection, and should have its own URI. Sending an HTTP GET request to the collection URI retrieves a list of items in the collection. Each item in the collection also has its own unique URI. An HTTP GET request to the item's URI returns the details of that item.

Adopt a consistent naming convention in URIs,it helps to use plural nouns for URIs that reference collections. It's a good practice to organize URIs for collections and items into a hierarchy.Also consider the relationships between different types of resources and how you might expose these associations.
Another factor is that all web requests impose a load on the web server. The more requests, the bigger the load. Therefore, try to avoid "chatty" web APIs that expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. Instead, you might want to denormalize the data and combine related information into bigger resources that can be retrieved with a single request. However, you need to balance this approach against the overhead of fetching data that the client doesn't need. Retrieving large objects can increase the latency of a request and incur additional bandwidth costs. Avoid introducing dependencies between the web API and the underlying data sources.

it might not be possible to map every operation implemented by a web API to a specific resource. You can handle such non-resource scenarios through HTTP requests that invoke a function and return the results as an HTTP response message.

# Define API operations in terms of HTTP methods :
The HTTP protocol defines a number of methods that assign semantic meaning to a request. The common HTTP methods used by most RESTful web APIs are:
  1. GET retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.
  2. POST creates a new resource at the specified URI. The body of the request message provides the details of the new resource.
  3. PUT either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.
  4. PATCH performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.
  5. DELETE removes the resource at the specified URI.

# The differences between POST, PUT, and PATCH  :
1.  POST :
           A POST request creates a resource. The server assigns a URI for the new resource, and returns that URI to the client. In the REST model, you frequently apply POST requests to collections. The new resource is added to the collection. A POST request can also be used to submit data for processing to an existing resource, without any new resource being created.
2.  PUT : 
           PUT request creates a resource or updates an existing resource. The client specifies the URI for the resource. The request body contains a complete representation of the resource. If a resource with this URI already exists, it is replaced. Otherwise a new resource is created, if the server supports doing so. PUT requests are most frequently applied to resources that are individual items, such as a specific customer, rather than collections. A server might support updates but not creation via PUT.
3. PATCH : 
           PATCH request performs a partial update to an existing resource. The client specifies the URI for the resource. The request body specifies a set of changes to apply to the resource. This can be more efficient than using PUT, because the client only sends the changes, not the entire representation of the resource.

# Media types :
clients and servers exchange representations of resources. For example, in a POST request, the request body contains a representation of the resource to create. In a GET request, the response body contains a representation of the fetched resource.In the HTTP protocol, formats are specified through the use of media types, also called MIME types.The Content-Type header in a request or response specifies the format of the representation. A client request can include an Accept header that contains a list of media types the client will accept from the server in the response message.

# GET methods :
A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).

# POST methods:
If a POST method creates a new resource, it returns HTTP status code 201 (Created). The URI of the new resource is included in the Location header of the response. The response body contains a representation of the resource.If the client puts invalid data into the request, the server should return HTTP status code 400 (Bad Request). The response body can contain additional information about the error or a link to a URI that provides more details.
If the method does some processing but does not create a new resource, the method can return HTTP status code 200 and include the result of the operation in the response body. Alternatively, if there is no result to return, the method can return HTTP status code 204 (No Content) with no response body.

# DELETE methods :
f the delete operation is successful, the web server should respond with HTTP status code 204, indicating that the process has been successfully handled, but that the response body contains no further information. If the resource doesn't exist, the web server can return HTTP 404 (Not Found).

# Asynchronous operations :
a POST, PUT, PATCH, or DELETE operation might require processing that takes a while to complete. If you wait for completion before sending a response to the client, it may cause unacceptable latency. If so, consider making the operation asynchronous. Return HTTP status code 202 (Accepted) to indicate the request was accepted for processing but is not completed.You should expose an endpoint that returns the status of an asynchronous request, so the client can monitor the status by polling the status endpoint. Include the URI of the status endpoint in the Location header of the 202 response.

# Filter and paginate data :
Exposing a collection of resources through a single URI can lead to applications fetching large amounts of data when only a subset of the information is required.Instead, the API can allow passing a filter in the query string of the URI, such as /orders?minCost=n. The web API is then responsible for parsing and handling the minCost parameter in the query string and returning the filtered results on the server side.
GET requests over collection resources can potentially return a large number of items. You should design a web API to limit the amount of data returned by any single request. Consider supporting query strings that specify the maximum number of items to retrieve and a starting offset into the collection.

# Support partial responses for large binary resources :
A resource may contain large binary fields, such as files or images. To overcome problems caused by unreliable and intermittent connections and to improve response times, consider enabling such resources to be retrieved in chunks. To do this, the web API should support the Accept-Ranges header for GET requests for large resources. This header indicates that the GET operation supports partial requests. The client application can submit GET requests that return a subset of a resource, specified as a range of bytes.onsider implementing HTTP HEAD requests for these resources. A HEAD request is similar to a GET request, except that it only returns the HTTP headers that describe the resource, with an empty message body. A client application can issue a HEAD request to determine whether to fetch a resource by using partial GET requests.

# Use HATEOAS to enable navigation to related resources :
HATEOAS: One of the primary motivations behind REST is that it should be possible to navigate the entire set of resources without requiring prior knowledge of the URI scheme. Each HTTP GET request should return the information necessary to find the resources related directly to the requested object through hyperlinks included in the response, and it should also be provided with information that describes the operations available on each of these resources. 

# URI versioning :
Each time you modify the web API or change the schema of resources, you add a version number to the URI for each resource. The previously existing URIs should continue to operate as before, returning resources that conform to their original schema.This versioning mechanism is very simple but depends on the server routing the request to the appropriate endpoint. 

# Query string versioning :
Rather than providing multiple URIs, you can specify the version of the resource by using a parameter within the query string appended to the HTTP request,The version parameter should default to a meaningful value such as 1 if it is omitted by older client applications.This approach has the semantic advantage that the same resource is always retrieved from the same URI, but it depends on the code that handles the request to parse the query string and send back the appropriate HTTP response. This approach also suffers from the same complications for implementing HATEOAS as the URI versioning mechanism.

# Header versioning :
Rather than appending the version number as a query string parameter, you could implement a custom header that indicates the version of the resource. This approach requires that the client application adds the appropriate header to any requests, although the code handling the client request could use a default value (version 1) if the version header is omitted. The following examples use a custom header named Custom-Header. The value of this header indicates the version of web API.

# Open API Initiative :
as created by an industry consortium to standardize REST API descriptions across vendors. As part of this initiative, the Swagger 2.0 specification was renamed the OpenAPI Specification (OAS) and brought under the Open API Initiative.You may want to adopt OpenAPI for your web APIs. Some points to consider:

   1. The OpenAPI Specification comes with a set of opinionated guidelines on how a REST API should be designed. That has advantages for interoperability, but requires more care when designing your API to conform to the specification.
   2. OpenAPI promotes a contract-first approach, rather than an implementation-first approach. Contract-first means you design the API contract the interface first and then write code that implements the contract.
   3. Tools like Swagger can generate client libraries or documentation from API contracts.































