#### Parser Content
```Java
{
Name = darktrace-darktrace-json-alert-trigger-breachurl
  Vendor = Darktrace
  Product = Darktrace
  TimeFormat = "epoch"
  Conditions = [ """darktrace """, """"severity":""", """"breachUrl""" ]
  Fields = [
    """"logsource":"({host}[^"]+)""",
    """"host"*:"*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?))"*,""",
    """"severity":({alert_severity}\d+)""",
    """"time\\?":({time}\d{13})""",
    """"breachUrl\\?":\\?"({malware_url}[^"\\]+)""",
    """"model\\?":\{[^\}]*?"name\\?":\\?"({alert_name}[^"\\]+)""",
    """"type":"({alert_type}[^"]+)""",
    """"description\\?":\\?"({additional_info}[^"]+)""",
    """"os":"({os}[^"]+)""",
    """"typelabel\\?":\\?"({device_type}[^\\"]+)""",
    """"macaddress\\?":\\?"({src_mac}[^"\\]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```