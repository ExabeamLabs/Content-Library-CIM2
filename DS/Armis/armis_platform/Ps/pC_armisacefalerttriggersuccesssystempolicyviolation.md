#### Parser Content
```Java
{
Name = armis-a-cef-alert-trigger-success-systempolicyviolation
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """device_0_type"""", """device_0_model"""" ,""""type":"System Policy Violation""""  ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """({alert_type}System Policy Violation)""",
    """title"\s*:\s*"({alert_name}[^"]+)""",
    """severity":"({alert_severity}[^"]+)""",
    """status":"({alert_status}[^"]+)""",
    """"deviceIds":\[({device_id_list}[^\]]+)""",
    """"device_0_ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"device_0_id":({device_id}\d+)""",
    """"device_0_name":"({device_name}[^"]+)""",
    """"device_0_category":"({device_category}[^"]+)""",
    """"device_0_riskLevel":({severity}\d+)""",
    """"device_0_model":"({device_model}[^"]+)""",
    """"device_0_sensorName":"({sensor}[^"]+)""",
    """"device_0_type":"({device_type}[^"]+)""",
    """"device_1_ipAddress":"({device_1_src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """"device_1_id":({device_1_id}\d+)""",
    """"device_1_name":"({device_1_name}[^"]+)""",
    """"device_1_category":"({device_1_category}[^"]+)""",
    """"device_1_riskLevel":({device_1_severity}\d+)""",
    """"device_1_model":"({device_1_model}[^"]+)""",
    """"device_1_sensorName":"({device_1_sensor}[^"]+)""",
    """"device_1_type":"({device_1_type}[^"]+)""",
    ]
  DupFields = ["device_name->src_host"]


}
```