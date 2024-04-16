#### Parser Content
```Java
{
Name = armis-a-cef-alert-trigger-success-systempolicyviolation-1
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """policyTitle"""", """alertId"""" ,""""severity"""", """"type":"System Policy Violation""""  ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """({alert_type}System Policy Violation)""",
    """title"\s*:\s*"({alert_name}[^"]+)""",
    """severity":"({alert_severity}[^"]+)""",
    """status":"({alert_status}[^"]+)""",
    """"alertId":({alert_id}\d+)"""
    """"description":"({additional_info}[^"]+)""""
  ]
  

}
```