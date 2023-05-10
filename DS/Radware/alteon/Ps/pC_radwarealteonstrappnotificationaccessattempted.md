#### Parser Content
```Java
{
Name = radware-alteon-str-app-notification-accessattempted
  Vendor = Radware
  Product = Alteon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ParserVersion = v1.0.0
  Conditions = [
    """: Access attempted by unauthorized """,
    """from host""",
    """>: """
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+({alert_type}\S+)\s+({app}\S+)\s+""",
    """({alert_name}({operation}Access attempted).+?)\s*$""",
    """from host (({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}\S+))"""
  ]
  DupFields = [ "alert_name->additional_info" ]


}
```