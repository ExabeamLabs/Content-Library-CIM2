#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-7398
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  Conditions = [ """%APF-4-MOBILESTATION_NOT_FOUND""", """apf_ms.c:7398""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-network-template.Fields} [
    """({additional_info}Could not find the mobile ({src_mac}[a-fA-F\d:.]+) in internal database)"""
  ]

cisco-network-template = {
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%(APF|DOT1X)-({priority}\d+)-({event_name}[^:]+):\s\w+\.c:({event_code}\d+)"""
  
}
```