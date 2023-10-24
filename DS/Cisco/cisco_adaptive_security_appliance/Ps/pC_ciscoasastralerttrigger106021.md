#### Parser Content
```Java
{
Name = cisco-asa-str-alert-trigger-106021
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-106021""", """%ASA-""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*%ASA-({priority}\d+)""",
    """({event_code}106021)""",
    """({event_name}Deny ICMP reverse path check)""",
    """%ASA\-\d+\-\d+:\s*Deny ({protocol}\w+)""",
    """from (({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)) to (({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)) on interface ({dest_interface}\S+)"""
  ]
  ParserVersion = "v1.0.0"


}
```