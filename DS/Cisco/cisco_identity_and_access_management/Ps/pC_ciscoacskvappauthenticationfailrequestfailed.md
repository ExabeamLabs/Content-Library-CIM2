#### Parser Content
```Java
{
Name = cisco-acs-kv-app-authentication-fail-requestfailed
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """Component=TacacsServer""", """Action=Failed""", """TACACS request from unknown""", """Level=ERROR""" ]
  Fields = [
    """Timestamp=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d\d\d\s\w{3})""",
    """Action=({result}[^,]+)""",
    """Description=({event_name}[^=]+)\s\w+=""",
    """,\d{1,3}\s({host}[\w\-.]+)\s"""
  ]


}
```