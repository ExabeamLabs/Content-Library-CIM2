#### Parser Content
```Java
{
Name = cisco-asa-kv-app-notification-734001
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-734001""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """User ({user}[^\s@,]+)(@({email_domain}[^\s@,]+))?""",
    """Addr (({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """({event_name}The following DAP records were selected)"""
  ]


}
```