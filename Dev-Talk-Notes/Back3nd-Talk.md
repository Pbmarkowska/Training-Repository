### Idempotency

It’s the ability to perform the same action multiple times while only producing “side effects” on the server once.

Side effects are defined as changes to the persistent data on the server.

Properly implemented `GET` requests are only used to retrieve data from the server, never to make changes to it, so they're naturally idempotent. This is a special case called being **safe**.

Safe methods are methods that are idempotent because they never produce any side effects. The HTTP `OPTIONS` and `HEAD` verbs also share this property.

There are two HTTP verbs which are idempotent but unsafe, the `PUT` and `DELETE` methods


Since our example API client is effectively read-only (only makes `GET` requests), we can use a "dumb" retry mechanism that simply re-sends requests until one succeeds or we exceed our maximum allowed number of retries.

Constructing a retry mechanism for non-idempotent requests requires cooperation from the server. Namely, the client attaches a unique ID to each request (a GUID/UUID would suffice). When the server processes a request successfully, it saves the ID and a copy of the response it wants to send back. If that response never makes it back to the client, the client will send the request again, reusing the same ID. The server will recognize the ID, skip the actual processing of the request, and just send back the stored response.

[source: _Idempotency, APIs, and Retries — Oh My!_ by Roger Jin ](https://hackernoon.com/idempotency-apis-and-retries-34b161f64cb4)

| HTTP Method   | Idempotent? | Safe? |
| ---|---|---|
|OPTIONS | yes | yes|
|GET  | yes | yes|
|HEAD | yes| yes|
|PUT| yes | no|
|POST| no| no|
|DELETE| yes| no|
|PATCH| no| no|

#### UUID - universally unique identifier <br>
Unikalna wartość

#### Optimistic and Pesimistic approach <br>
