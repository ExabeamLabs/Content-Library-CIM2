#### Parser Content
```Java
{
Name = "fortinet-fortiauthenticator-kv-app-logout-authentication"
  Vendor = "Fortinet"
  Product = "FortiAuthenticator"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """subcategory="Authentication"""", """action="Logout"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """nas="({dest_host}[^"]+)"""",
    """user="({user}[^"]+)"""",
    """action="({event_name}[^"]+)"""",
    """status="[^"]*" ({description}.+?)\s*$""",
  ]


}
```