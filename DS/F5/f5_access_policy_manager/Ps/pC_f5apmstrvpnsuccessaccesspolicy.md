#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-accesspolicy
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Common:""", """Access policy result:""" ]
  Fields = [
    """:Common:({session_id}[^\s:]+): Access policy result""",
    """\sAccess policy result:\s*({policy_name}[^"]+?)\s*("|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```