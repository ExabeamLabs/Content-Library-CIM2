#### Parser Content
```Java
{
Name = entrust-ie-str-space-delimited-app-authentication-fail-foruser
  Vendor = Entrust
  Product = Entrust Identity Enterprise
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """An invalid response was specified for the token with serial number """ , """ for user """ ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
    """({additional_info}An invalid response was specified for the token with serial number .+)""",
    """for user (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\.""",

  ]


}
```