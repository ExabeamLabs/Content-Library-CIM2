#### Parser Content
```Java
{
Name = cisco-asa-kv-network-session-fail-750003
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-750003""", """%ASA-""" ]
  Fields = [
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """Local:(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)):({dest_port}\d+)""",
    """Remote:(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)):({src_port}\d+)""",
    """Username:({user}.*?)\s+({protocol}\w+)?\s*({event_name}Negotiation aborted due to ERROR)""",
    """ERROR:\s*(|({failure_reason}.*?))\s*$"""
  ]


}
```