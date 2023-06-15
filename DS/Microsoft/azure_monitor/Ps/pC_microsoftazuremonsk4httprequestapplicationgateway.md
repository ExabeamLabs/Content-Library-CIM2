#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-applicationgateway
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """requestClientApplication=Azure""", """"category": "ApplicationGatewayAccessLog"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"time": "({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"operationName": "({operation}[^"]+)"""",
    """originalHost":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^"]+))"""",
    """"userAgent":"(-|({user_agent}[^"]+))"""",
    """requestUri":"({request_uri}[^"]+)"""",
    """receivedBytes":"*({bytes_in}\d+)""",
    """sentBytes":"*({bytes_out}\d+)""",
    """"httpMethod":"({method}[^"]+)"""",
    """"httpStatus":({http_response_code}\d+)""",
    """"httpVersion":"({protocol}\w+)""",
    """"resourceId": "({object}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```