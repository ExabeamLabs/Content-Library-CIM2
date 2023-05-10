#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-success-713903
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """-713903""", """%ASA-""" ]
  Fields = [
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """%ASA\-\d+\-\d+:\s*({module}.*?):\s*Runt\s*({protocol}\w+)\s*({event_name}.*?)\s*\d+""",
    """from\s*(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)):({src_port}\d+)"""
  ]


}
```