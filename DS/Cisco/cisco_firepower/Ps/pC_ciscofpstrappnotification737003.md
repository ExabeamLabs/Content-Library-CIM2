#### Parser Content
```Java
{
Name = cisco-fp-str-app-notification-737003
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
  """-737003"""
  """%FTD-"""
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """:\s+Session=({session_id}[^\s,]+)""",
    """({event_name}DHCP configured, no viable servers found)""",
  ]


}
```