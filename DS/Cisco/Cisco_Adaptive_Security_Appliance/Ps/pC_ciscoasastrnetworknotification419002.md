#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-419002
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-419002""" ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)""",
    """(\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)\s+({host}[\w\.-]+)\s*:\s*%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """-419002:\s*({event_name}.*?) from """,
    """\sfrom\s+({src_interface}.+?):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+)\s+)|\s+)""",
    """\sto\s+({dest_interface}.+?):(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+))|\s+)""",
    """ with ({failure_reason}.*?)\s*$"""
  ]


}
```