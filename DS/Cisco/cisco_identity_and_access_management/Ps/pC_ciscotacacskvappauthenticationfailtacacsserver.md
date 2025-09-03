#### Parser Content
```Java
{
Name = cisco-tacacs-kv-app-authentication-fail-tacacsserver
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """Component=TacacsServer""", """Action=Failed""", """Authorization request""" ]
  Fields = [
    """Timestamp=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d\d\d\s\w{3})""",
    """,\d{1,3}\s({host}[\w\-.]+)\s""",
    """Action=({result}[^,]+)""",
    """Description=({event_name}[^=]+)\s\w+=""",
    """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]


}
```