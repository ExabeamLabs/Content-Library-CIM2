#### Parser Content
```Java
{
Name = cisco-securenwanalytics-str-alert-trigger-success-z
  Vendor = Cisco
  Product = Cisco Secure Network Analytics
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """StealthWatch[""", """]: """ , """Z;""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z);[^;]*;(|({alert_name}[^;]+));[^;]*;(|({alert_type}[^;]+));({alert_severity}[^;]+);[^;]*;(|({additional_info}[^;]+));(|0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);(|({src_host}[\w\-.]+));(|0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?);(|({dest_host}[\w\-.]+));([^;]*;){3}(|({host}[A-Fa-f:\d.]+));(|({=host}[\w\-.]+));""",
  ]
  ParserVersion = "v1.0.0"


}
```