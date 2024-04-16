#### Parser Content
```Java
{
Name = apc-a-str-app-login-fail-invalidcredentials
  Vendor = APC
  Product = APC
  TimeFormat = "ddMMMyy HH:mm:ss"
  Conditions = [ """Invalid login credentials;""", """user: """" ]
  Fields = [
    """\s\w\w\w\s({time}\d{1,2}\w{1,3}\d\d\s\d\d:\d\d:\d\d)\s""",
    """user:\s"({user}[\w\.\-]{1,40}\$?)"""",
    """({failure_reason}Invalid login credentials)"""
    ]
  ParserVersion = "v1.0.0"


}
```