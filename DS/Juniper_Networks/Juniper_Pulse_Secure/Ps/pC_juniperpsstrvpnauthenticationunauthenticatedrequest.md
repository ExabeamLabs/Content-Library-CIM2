#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-authentication-unauthenticatedrequest
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ PulseSecure: - - ""","""- Unauthenticated request url """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s\S+\s\S+\s\S+\s\[({host}[\w\-.]+)\]\s(System|({user}[^(\s]+))""",
    """({operation}Unauthenticated request url)\s({uri_path}\/[^\?\s]*?)(\?({uri_query}\S+))?\s""",
    """IP\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """({app}PulseSecure)"""
  ]
  ParserVersion = "v1.0.0"


}
```