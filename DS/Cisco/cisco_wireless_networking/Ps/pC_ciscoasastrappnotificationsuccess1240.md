#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-1240
  ParserVersion = v1.0.0
  Product = Cisco Wireless Networking
  Conditions = [ """%APF-6-GUEST_ASSIGNED_IP""", """apf_foreignap.c:1240""", """ assigned IP Address """ ]
  Fields = ${DLCiscoParsersTemplates.cisco-network-template.Fields} [
    """({additional_info}Guest User \([^\)]*\) with MAC Address \(({src_mac}[a-fA-F\d:.]+)\) assigned IP Address \([^\)]+\))"""
  ]

cisco-network-template = {
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%(APF|DOT1X)-({priority}\d+)-({event_name}[^:]+):\s\w+\.c:({event_code}\d+)"""
  
}
```