#### Parser Content
```Java
{
Name = entrust-ie-str-app-authentication-success-igradiusapiauthenticate
  Vendor = Entrust
  Product = Entrust Identity Enterprise
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ [IG.SYSTEM.IGRadius.API] Authenticate """ , """ response for user """ ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """ response for user (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+))""",
    """\[({event_name}IG.SYSTEM.IGRadius.API)\] ({event_description}Authenticate .+)"""
  ]


}
```