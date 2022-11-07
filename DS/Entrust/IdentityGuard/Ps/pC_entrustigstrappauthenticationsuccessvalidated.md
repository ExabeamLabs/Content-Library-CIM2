#### Parser Content
```Java
{
Name = entrust-ig-str-app-authentication-success-validated
  Vendor = Entrust
  Product = IdentityGuard
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [AuthenticationManager:authenticateGeneric:user] """ , """ validated""" ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """ \[({event_name}AuthenticationManager:authenticateGeneric:user)\] (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+))\s""",
  ]


}
```