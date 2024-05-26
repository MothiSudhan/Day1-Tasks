_# Difference between HTTP1.1 vs HTTP2_

| HTTP 1                                                                                                        | HTTP 2                                                                          |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| It works on the textual format.                                                                               | It works on the binary protocol.                                                |
| There is head of line blocking that blocks all the requests behind it until it doesn’t get its all resources. | It allows multiplexing so one TCP connection is required for multiple requests. |
| It uses requests resource Inlining for use getting multiple pages.                                            | It uses PUSH frame by server that collects all multiple pages.                  |
| It compresses data by itself.                                                                                 | It uses HPACK for data compression.                                             |
| One connection per request.The next request slows down until the first response is sent.                      | Uses multiplexing which allows multiple request under single TCP                |

|Headers are sent repeatedly for each request and response even while requesting to the
same server.|Includes header compression, which reduces size of data and time consumed by compressing
repeated headers.|
|Client cannot prioritize the certain stream or resources they want. |This allows to prioritize individual resources which enables efficient
resource allocation ensuring critical resources are downloaded first.|
|This allows to prioritize individual resources which enables efficient
resource allocation ensuring critical resources are downloaded first.|Has server push feature which proactively pushes the resources to the clients
before the request reduing the loading time and eliminating the round trip of
fetching required resources again after request|
