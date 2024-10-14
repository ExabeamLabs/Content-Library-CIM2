#### Parser Content
```Java
{
Name = entrust-ie-str-app-authentication-success-validated
  Vendor = Entrust
  Product = Entrust Identity Enterprise
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [AuthenticationManager:authenticateGeneric:user] """ , """ validated""" ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """ \[({event_name}AuthenticationManager:authenticateGeneric:user)\] (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
  ]


}
```