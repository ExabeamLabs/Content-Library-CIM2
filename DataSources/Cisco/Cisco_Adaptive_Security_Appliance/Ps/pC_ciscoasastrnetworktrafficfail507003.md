#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-507003
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-507003""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+):\s*({protocol}\S+)""",
    """from\s+({src_interface}[^:]+):\s*(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)""",
    """to\s+({dest_interface}[^:]+):\s*(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)""",
    """({event_name}terminated by inspection engine)""",
    """reason\s*\-\s*({failure_reason}[^"]+?)\s*("|$)"""
  ]


}
```