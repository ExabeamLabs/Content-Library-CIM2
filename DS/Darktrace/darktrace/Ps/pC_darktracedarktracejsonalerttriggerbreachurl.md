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
    """"host"*:"*(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}.+?))"*,""",
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