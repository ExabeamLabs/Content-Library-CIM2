#### Parser Content
```Java
{
Name = entrust-ig-str-app-authentication-fail-failedauthentication
  Vendor = Entrust
  Product = IdentityGuard
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [IG.SYSTEM.AuthenticationManagement.API] user """ , """ failed authentication""" ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """({event_name}IG.SYSTEM.AuthenticationManagement.API)""",
    """ user (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+)) failed authentication""",
  ]


}
```