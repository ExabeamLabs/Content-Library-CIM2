#### Parser Content
```Java
{
Name = radware-alteon-str-app-notification-notsynchronized
  Vendor = Radware
  Product = Alteon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """: Configuration is not synchronized """, """>: """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+({alert_type}\S+)\s+({app}\S+)\s+""",
    """({operation}Switch HA)""",
    """({additional_info}Configuration is not synchronized between the HA devices)"""
  ]


}
```