## Difference between HTTP 1.1 vs HTTP 2

| HTTP 1                                                                                                        | HTTP 2                                                                                                     |
| ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| It works on the textual format.                                                                               | It works on the binary protocol.                                                                           |
| There is head of line blocking that blocks all the requests behind it until it doesn’t get its all resources. | It allows multiplexing so one TCP connection is required for multiple requests.                            |
| It uses requests resource Inlining for use getting multiple pages.                                            | It uses PUSH frame by server that collects all multiple pages.                                             |
| It compresses data by itself.                                                                                 | It uses HPACK for data compression.                                                                        |
| One connection per request.The next request slows down until the first response is sent.                      | Uses multiplexing which allows multiple request under single TCP                                           |
| Headers are sent repeatedly for each request and response even while requesting to the same server.           | Includes header compression, which reduces size of data and time consumed by compressing repeated headers. |
| Client cannot prioritize the certain stream or resources they want.                                           | This allows to prioritize individual resources which enables efficient                                     |
 resource allocation ensuring critical resources are downloaded first.                                        



## Objects and its internal representation in JavaScript.

- Objects are data types in javascript.
- Objects are different than primitive datatypes (i.e. number, string, boolean, etc.)
- Primitive data types contain one value but Objects can hold many values in form of Key: value pair.
- These keys can be variables or functions and are called properties and methods, respectively, in the context of an object.
- Every object has some property associated with some value. These values can be accessed using these properties associated with them.

ex.,
var person=
{
name:"praveena",
age:26,
address:"palani,tamil nadu",
brother:"vishnu",
marrital status: "true",
fathername:"natarajan",
mothername:"banu"

}
console.log(person)
