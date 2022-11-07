#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-713228
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """Assigned private IP address""", """-713228""","""%ASA-""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d+:\d+:\d+):""",
    """%ASA-({priority}\d+)-({event_code}\d+): Group =\s*({realm}[^,]+),\s*Username = ({user}[^,@]+?),?\s+IP = ({src_ip}[^\s,]+)[,\s]+Assigned private IP address ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) to"""
  ]


}
```