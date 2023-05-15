#### Parser Content
```Java
{
Name = secureauth-login-leef-app-logout-90050
  ParserVersion = "v1.0.0"
  Vendor = SecureAuth
  Product = SecureAuth Login
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """EventID="90050"""", """Session - End""", """ApplianceID=""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
    """\sHostName ="({host}[\w\-.]+)"""",
    """\sCategory="({category}[^"]+)"""",
    """({event_code}90050)""",
    """({event_name}Session - End)""",
    """\sUserID="+(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """\WAppliance="({dest_host}[\w\-.]+)""",
    """\WRealm="({realm}[^"]+)""",
    """\WPriority="({priority}\d+)"""
  ]


}
```