#### Parser Content
```Java
{
Name = armis-a-json-alert-trigger-success-systempolicyviolation
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"alertId": """, """"activities": """, """"status": """, """"type": "System Policy Violation""""  ]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """({alert_type}System Policy Violation)""",
    """title"\s*:\s*"({alert_name}[^"]+)""",
    """severity"\s*:\s*"({alert_severity}[^"]+)""",
    """status"\s*:\s*"({alert_status}[^"]+)""",
    """description"\s*:\s*"({additional_info}[^"]+)""",
    """alertId"\s*:\s*({alert_id}\d+)""",
    """"deviceIds"\s*:\s*\[({device_id_list}[^\]]+)"""
    ]


}
```