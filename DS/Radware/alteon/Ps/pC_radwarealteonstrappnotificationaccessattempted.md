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
    """from host (({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}\S+))"""
  ]
  DupFields = [ "alert_name->additional_info" ]


}
```