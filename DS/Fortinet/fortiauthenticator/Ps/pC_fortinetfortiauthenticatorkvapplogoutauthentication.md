#### Parser Content
```Java
{
Name = "fortinet-fortiauthenticator-kv-app-logout-authentication"
  Vendor = "Fortinet"
  Product = "FortiAuthenticator"
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ """subcategory="Authentication"""", """action="Logout"""" ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """nas="({dest_host}[^"]+)"""",
    """user="({user}[\w\.\-]{1,40}\$?)"""",
    """action="({event_name}[^"]+)"""",
    """status="[^"]*" ({description}.+?)\s*$""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]


}
```