#### Parser Content
```Java
{
Name = f5-bigipdns-str-http-request-success-proxyrequest
  Vendor = F5
  Product = F5 BIG-IP DNS
  ParserVersion = "v1.0.0"
  TimeFormat = "dd/MMM/yyyy HH:mm:ss Z"
  Conditions = [ """ <HTTP_PROXY_REQUEST>:""", """]: Rule""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s({event_category}\w+)\s""",
    """:\s+Rule\s+({rule}[^\s]+)""",
    """<HTTP_PROXY_REQUEST>:\s({additional_info}[^"$]+?)\s?("|$)"""
  ]


}
```