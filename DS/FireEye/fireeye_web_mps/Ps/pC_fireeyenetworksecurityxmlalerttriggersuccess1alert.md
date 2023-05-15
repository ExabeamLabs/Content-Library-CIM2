#### Parser Content
```Java
{
Name = fireeye-networksecurity-xml-alert-trigger-success-1alert
  Vendor = FireEye
  Product = FireEye Web MPS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """.1.alert:""","""msg="extended"""","""product="Web MPS""" ]
  Fields = [
    """<occurred>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """<alert id="({alert_id}[^"]+)""",
    """<malware name="({alert_name}[^"]+)"""",
    """xsi:schemaLocation=.+?name="({alert_type}[^"]+)".*severity="({alert_severity}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```