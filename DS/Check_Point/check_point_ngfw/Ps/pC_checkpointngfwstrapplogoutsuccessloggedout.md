#### Parser Content
```Java
{
Name = checkpoint-ngfw-str-app-logout-success-loggedout
  ParserVersion = "v1.0.0"
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]: """ , """][""", """ logged out """ ]
  Fields = [
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[[^\]]*\]\[[^\]]*\]\[[^\]]*\]\s*<\d+>(({src_host}[\w\-.]+)\s+)?({process_name}.+?)\[({process_id}\d+)\]:\s*({additional_info}User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+logged out.*?)\s*$""",
  ]
}  

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