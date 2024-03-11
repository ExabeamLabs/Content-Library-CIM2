#### Parser Content
```Java
{
Name = cisco-asa-str-process-create-success-111010
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-111010""", """%ASA-""" ]
  Fields = [
   """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """User\s+'(({domain}[^\\']+)\\+)?({user}[^']+)'""",
    """({event_name}executed)\s+'({process_command_line}[^']+)\s*'""",
    """from IP ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```