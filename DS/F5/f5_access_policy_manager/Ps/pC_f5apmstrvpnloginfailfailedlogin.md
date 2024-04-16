#### Parser Content
```Java
{
Name = f5-apm-str-vpn-login-fail-failedlogin
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Common:""", """AD Agent:""" ]
  Fields = [
    """:Common:({session_id}[^\s:]+): AD Agent:""",
    """AD Agent:\s*({failure_reason}[^"]+?)\s*("|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```