#### Parser Content
```Java
{
Name = avinetworks-lb-str-app-login-success-loginsuccess
  Vendor = AVI Networks
  Product = Load Balancer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Avi-Controller:""", """event USER_LOGIN occurred""", """login (Success) from""" ]
  Fields = [
    """At\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """User\s({user}[^\s]+)""",
    """from\s({src_ip}[a-fA-F\d\.:]+)""",
    """event\s({event_name}USER_LOGIN)""",
    """login\s\(({result}Success)\)""",
    """object\s({object}[^\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```