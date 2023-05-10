#### Parser Content
```Java
{
Name = cisco-asa-str-arp-traffic-405001
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-405001""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """from\s+(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_mac}[^\/\s]+)\s*on interface\s+({dest_interface}\S+) with ({reason}.+?)\s*(((\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|([^\s]+?))\/([^\/\s]+)"""
# DL Fields are removed
    """({event_name}Received ARP response collision)""",
    """({protocol}ARP)"""
  ]


}
```