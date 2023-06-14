#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-notification-serverdown
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """,SYSTEM,auth,""", """,auth-server-down,""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),""",
    """,auth-server-down,([^,]*,){4}({alert_severity}[^,]+),"({additional_info}[^"]+)\s"""",
    """,SYSTEM,auth,([^,]*,){3}({alert_name}[^,]+),""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```