#### Parser Content
```Java
{
Name = mcafee-es-cef-alert-trigger-success-roguesystemdetected
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch"
  Conditions = [ """CEF""", """|McAfee|Rogue System Sensor|""", """|Rogue System|""", """Detected Rogue System""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wagt=({host}.+?)\s+(\w+=|$)""",
    """\Wcs6=({additional_info}.+?)\s+(\w+=|$)""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wcs4=({os}.+?)\s+(\w+=|$)""",
    """\Wseverity=({alert_severity}.+?)\s+(\w+=|$)""",
    """\WcategoryTechnique=({threat_category}.+?)\s+(\w+=|$)""",
    """CEF:([^\|]*\|){4}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_type}[^\|]+)""",
  ]


}
```