## REST
REpresentation State Transfer (REST) is an architectural style inspired by the Web. 
Most important is the concept of resources. You can think of a resource as a thing that the service itself knows about, like a Customer. The server creates different representations of this Customer on request. How a resource is shown externally is completely decoupled from how it is stored internally. A client might as JSON representation of a Customer, for example, even if it is stored in a completely different format. Once a client has a representation of this Customer, it can then make requests to change it, and the server may or may not comply with them.

#### REST and HTTP
HTTP has built-in features that work well with the REST style. For example, HTTP verbs like GET, POST, and PUT already have clear meanings. REST says that these methods should behave the same way for all resources. For instance, GET retrieves data without changing it (idempotent), and POST is used to create new data. So, instead of having separate methods like `createCustomer` or  `editCustomer`, we can just POST a customer to create it or GET one to retrieve it. This means there's mainly one endpoint (like `/customer`), and the action depends on the HTTP method used.

HTTP also comes with a big set of helpful tools and technologies. There are caching tools like Varnish, load balancers, and many monitoring tools that support HTTP by default. These tools help manage large amounts of traffic and direct it efficiently, making it easier to secure communications. However, you only get these benefits if you use HTTP correctly. If used poorly, it can be just as insecure or hard to scale as other systems. 

HTTP can also be used for RPC (Remote Procedure Calls), like with SOAP, but SOAP often ignore key HTTP features, such as using verbs properly or using standard error codes. Sometimes, instead of using existing standards, new ones are created that only work with new technologies. 

#### Downside of REST over HTTP
1. **Harder to auto-generate clients**: Unlike RPC, it's not easy to generate client stubs (ready-to-use client code) for REST over HTTP. This complexity often pushes people to misuse HTTP by building RPC-like systems or shared client libraries.

2. **Shared code can be risky**: Sharing code between client and server might seem convenient, but it can lead to problems; especially in microservices, because it tightly couples them.

3. **Note all frameworks support all HTTP verbs**: While verbs like GET and POST are widely supported, PUT and DELETE might need extra effort depending on the web framework. REST-specific frameworks handle this better.