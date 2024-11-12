# http-ws-reference

A simple reference for overlapping HTTP/WS close codes

[Inspiration](https://github.com/Luka967/websocket-close-codes)

[IANA Websocket Close Code Registry](https://www.iana.org/assignments/websocket/websocket.xhtml#close-code-number)

[Websocket Specification IETF](https://datatracker.ietf.org/doc/html/rfc6455#section-7.4)

| **Category**             | **HTTP Status Code** | **HTTP Status Text**          | **WebSocket Close Code** | **WebSocket Close Text**        | **Description**                                                                            |
|--------------------------|----------------------|--------------------------------|---------------------------|----------------------------------|------------------------------------------------------------------------------------------------|
| **Success/Normal Closure**         | 200                  | OK                             | 1000                      | Normal Closure                   | The request was successfully processed, or the connection was closed normally.                 |
| **No Status/No Response Received** | 204                  | No Content                    | 1005                      | No Status Received               | No additional information is provided, or no status was received.                             |
| **Protocol Error/Bad Request**     | 400                  | Bad Request                   | 1002                      | Protocol Error                   | The request contained malformed syntax or protocol violations.                                |
| **Invalid Data/Bad Request**       | 400                  | Bad Request                   | 1007                      | Invalid Frame Payload Data       | The server detected invalid data (e.g., invalid encoding) in the request or payload.          |
| **Unauthorized Access**            | 401                  | Unauthorized                  | 3000                      | Unauthorized                     | The client attempted an unauthorized action.                                                  |
| **Policy Violation/Forbidden**     | 403                  | Forbidden                     | 1008                      | Policy Violation                 | The request violated server policies, or access was forbidden.                                |
| **Unsupported Media Type/Unsupported Data** | 415         | Unsupported Media Type        | 1003                      | Unsupported Data                 | The client sent data that is not supported by the server.                                     |
| **Payload Too Large/Message Too Big** | 413             | Payload Too Large             | 1009                      | Message Too Big                  | The message/request size exceeds server limits.                                               |
| **Unsupported Extension/Required Extensions Not Met** | 426 | Upgrade Required          | 1010                      | Mandatory Extension              | The client expected a specific protocol extension that was not agreed upon.                   |
| **Bad Gateway/Gateway Timeout**    | 502                  | Bad Gateway                   | 1014                      | Bad Gateway                      | The server received an invalid response from an upstream server.                              |
| **Service Unavailable/Service Restart** | 503           | Service Unavailable           | 1012                      | Service Restart                  | The server is restarting, causing the connection to terminate.                                |
| **Service Unavailable/Try Again Later** | 503          | Service Unavailable           | 1013                      | Try Again Later                  | The server is currently overloaded; client should try again later.                            |
| **Handshake Error/TLS Required**   | 426                  | Upgrade Required              | 1015                      | TLS Handshake                    | The client attempted to connect without the required TLS handshake or protocol.               |
| **Internal Server Error**          | 500                  | Internal Server Error         | 1006                      | Abnormal Closure                 | The connection closed unexpectedly, likely due to an internal server error.                   |
| **Internal Server Error**          | 500                  | Internal Server Error         | 1011                      | Internal Error                   | The server encountered an unexpected condition, leading to an error.                          |
| **Custom/Private Codes**           | -                    | -                              | 4000-4999                 | Reserved for Private Use         | Both HTTP and WebSocket provide ranges for application-specific, non-standard error handling. |
