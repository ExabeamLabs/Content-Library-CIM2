#### Parser Content
```Java
{
Name = cisco-ise-kv-app-notification-success-authentication
  Conditions = [ """CISE_Alarm""", """Authentication Latency""" ]
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """CISE_Alarm ({event_category}[^:]+):\s*({event_name}.+?)\s*:""",
    """Server=({src_host}[\w\-\.]+)(?:;|$)""",
    """NAS IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:;|$)""",
  ]


}
```