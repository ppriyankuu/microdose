## REST
REpresentation State Transfer (REST) is an architectural style inspired by the Web. 
Most important is the concept of resources. You can think of a resource as a thing that the service itself knows about, like a Customer. The server creates different representations of this Customer on request. How a resource is shown externally is completely decoupled from how it is stored internally. A client might as JSON representation of a Customer, for example, even if it is stored in a completely different format. Once a client has a representation of this Customer, it can then make requests to change it, and the server may or may not comply with them.

#### REST and HTTP
HTTP has built-in features that work well with the REST style. For example, HTTP verbs like GET, POST, and PUT already have clear meanings. REST says that these methods should behave the same way for all resources. For instance, GET retrieves data without changing it (idempotent), and POST is used to create new data. So, instead of having separate methods like `createCustomer` or  `editCustomer`, we can just POST a customer to create it or GET one to retrieve it. This means there's mainly one endpoint (like `/customer`), and the action depends on the HTTP method used.

HTTP also comes with a big set of helpful tools and technologies. There are caching tools like Varnish, load balancers, and many monitoring tools that support HTTP by default. These tools help manage large amounts of traffic and direct it efficiently, making it easier to secure communications. However, you only get these benefits if you use HTTP correctly. If used poorly, it can be just as insecure or hard to scale as other systems. 

HTTP can also be used for RPC (Remote Procedure Calls), like with SOAP, but SOAP often ignore key HTTP features, such as using verbs properly or using standard error codes.

