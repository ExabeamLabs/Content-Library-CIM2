#### Parser Content
```Java
{
Name = entrust-ig-str-app-authentication-success-apiauthenticate
  Vendor = Entrust
  Product = IdentityGuard
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [IG.SYSTEM.AuthenticationManagement.API] authenticate """ ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """ \[({event_name}IG.SYSTEM.AuthenticationManagement.API)\] authenticate (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+))\s""",
  ]


}
```