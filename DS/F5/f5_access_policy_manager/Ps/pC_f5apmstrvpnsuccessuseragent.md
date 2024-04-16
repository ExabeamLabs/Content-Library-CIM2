#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-useragent
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """/Common/""", """:Common:""", """Received User-Agent header:""" ]
  Fields = [
    """:Common:({session_id}[^\s:]+): Received User-Agent header:""",
    """Received User-Agent header:\s*({user_agent}.+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```