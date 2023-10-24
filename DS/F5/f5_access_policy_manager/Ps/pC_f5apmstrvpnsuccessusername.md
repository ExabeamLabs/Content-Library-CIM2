#### Parser Content
```Java
{
Name = f5-apm-str-vpn-success-username
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Common:""", """Username """ ]
  Fields = [
    """:Common:({session_id}[^\s:]+): Username""",
    """\sUsername\s+'(?:[^'\\]+\\{1,20})?({user}[\w\.\-]{1,40}\$?)'"""
  ]
  ParserVersion = "v1.0.0"


}
```