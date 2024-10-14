#### Parser Content
```Java
{
Name = entrust-ie-str-app-authentication-success-apiauthtype
  Vendor = Entrust
  Product = Entrust Identity Enterprise
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [IG.SYSTEM.AuthenticationManagement.API] Authenticate type """ ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """({event_name}IG.SYSTEM.AuthenticationManagement.API)""",
    """Authenticate type ({auth_method}[^\s]+) for (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
  ]


}
```