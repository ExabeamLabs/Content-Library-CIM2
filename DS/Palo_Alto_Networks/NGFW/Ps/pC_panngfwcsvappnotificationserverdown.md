#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-notification-serverdown
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = NGFW
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,SYSTEM,auth,""", """,auth-server-down,""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),""",
    """,auth-server-down,([^,]*,){4}({alert_severity}[^,]+),"({additional_info}[^"]+)\s"""",
    """,SYSTEM,auth,([^,]*,){3}({alert_name}[^,]+),"""
  ]


}
```