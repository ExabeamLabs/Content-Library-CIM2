#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-5717
  ParserVersion = v1.0.0
  Product = Cisco Identity and Access Management
  Conditions = [ """%DOT1X-4-MAX_EAP_RETRIES""", """1x_auth_pae.c:5717""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-network-template.Fields} [
    """({additional_info}Max EAP identity request retries \(\d+\) exceeded for client ({src_mac}[a-fA-F\d:.]+))"""
  ]

cisco-network-template = {
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%(APF|DOT1X)-({priority}\d+)-({event_name}[^:]+):\s\w+\.c:({event_code}\d+)"""
  
}
```