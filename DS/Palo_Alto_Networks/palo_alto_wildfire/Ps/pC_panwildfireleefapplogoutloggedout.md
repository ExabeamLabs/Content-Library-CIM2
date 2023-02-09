#### Parser Content
```Java
{
Name = pan-wildfire-leef-app-logout-loggedout
  Vendor = Palo Alto Networks
  Product = Palo Alto WildFire
  ParserVersion = v1.0.0
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """|Palo Alto Networks|PAN-OS""", """ubtype=general|""", """logged out""" ]
  Fields = [
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """\|DeviceName =({host}[^\|]+?)\s*(\||$|")""",
    """\|msg="*({event_name}[^\|"]+)""",
    """\|Severity=({alert_severity}[^\|]+)""",
# flags is removed
    """User\s+({user}[^\s]+)"""
    ]


}
```