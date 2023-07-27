#### Parser Content
```Java
{
Name = envoy-e-json-http-session-http
  Vendor = Envoy
  Product = Envoy
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""""request":""",""""response":""",""""downstreamLocalAddress":""",""""downstreamDirectRemoteAddress":"""]
  Fields = [
    """"user":"({user}[\w\.\-]{1,40}\$?)"""",
    """"requestMethod":"({method}[^"]+)"""",
    """"requestBodyBytes":"({bytes_in}\d+)"""",
    """"responseBodyBytes":"({bytes_out}\d+)"""",
    """"responseCode":({http_response_code}\d+)""",
    """"protocolVersion":"({protocol}[A-Za-z]+)""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"downstreamLocalAddress":[^\}]+?"address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"downstreamLocalAddress":[^\}]+?"portValue":({src_port}\d+)""",
    """"upstreamRemoteAddress":[^\}]+?"portValue":({dest_port}\d+)""",
    """"upstreamRemoteAddress":[^\}]+?"address":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"responseCodeDetails":"({additional_info}[^"]+)""""
  ]


}
```