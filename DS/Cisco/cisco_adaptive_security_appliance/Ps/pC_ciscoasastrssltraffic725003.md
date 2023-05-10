#### Parser Content
```Java
{
Name = cisco-asa-str-ssl-traffic-725003
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
  """-725003"""
  """%ASA-"""
  ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*%ASA-({priority}\d+)"""
    """({event_code}725003)"""
    """({event_name}request to resume previous session)"""
    """({src_interface}[^\s]+):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))\/({src_port}\d+)"""
    """to\s*(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+))\/({dest_port}\d+)"""
  ]


}
```