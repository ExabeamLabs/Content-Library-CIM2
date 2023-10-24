#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-sessiondeleted
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """/Common/""", """:Common:""", """Session deleted""" ]
  Fields = [
    """:Common:({session_id}[^\s:]+): Session deleted""",
  ]
  ParserVersion = "v1.0.0"


}
```