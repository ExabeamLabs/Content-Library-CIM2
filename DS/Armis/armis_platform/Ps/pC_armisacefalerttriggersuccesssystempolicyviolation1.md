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
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({alert_type}System Policy Violation)""",
    """title"\s*:\s*"({alert_name}[^"]+)""",
    """severity":"({alert_severity}[^"]+)""",
    """status":"({alert_status}[^"]+)""",
    """"alertId":({alert_id}\d+)""",
    """"description":"({additional_info}[^"]+)"""",
    """"sourceEndpoints":\[\{[^\}]*?"ip":\[?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourceEndpoints":\[\{[^\}]*?"macAddress":\[?"({src_mac}[^"]+)"\]""",
    """"sourceEndpoints":\[\{[^\}]*?"name":"({src_host}[\w\-\.]+)"""",
    """"destinationEndpoints":\[\{[^\}]*?"name":"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+))"""",
    """"destinationEndpoints":\[\{[^\}]*?"ip":\[?"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"destinationEndpoints":\[\{[^\}]*?"macAddress":\[?"({dest_mac}[^"]+)""""
  ]
  

}
```