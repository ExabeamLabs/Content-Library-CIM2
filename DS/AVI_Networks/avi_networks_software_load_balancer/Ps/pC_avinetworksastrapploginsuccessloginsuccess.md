#### Parser Content
```Java
{
Name = avinetworks-a-str-app-login-success-loginsuccess
  Vendor = AVI Networks
  Product = AVI Networks Software Load Balancer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Avi-Controller:""", """event USER_LOGIN occurred""", """login (Success) from""" ]
  Fields = [
    """At\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """User\s({user}[\w\.\-]{1,40}\$?)""",
    """from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """event\s({event_name}USER_LOGIN)""",
    """login\s\(({result}Success)\)""",
    """object\s({object}[^\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```