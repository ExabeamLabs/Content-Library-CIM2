#### Parser Content
```Java
{
Name = cisco-asa-str-configuration-modify-8527
  ParserVersion = v1.0.0
  Product = Cisco Wireless Networking
  Conditions = [ """%APF-6-USER_NAME_CREATED""", """apf_ms.c:8527""", """Username entry""", """ created for mobile """ ]
  Fields = ${DLCiscoParsersTemplates.cisco-network-template.Fields} [
    """({additional_info}Username entry \([^\)]+\) with length \(\d+\) created for mobile ({src_mac}[a-fA-F\d:.]+))\s*"""
  ]

cisco-network-template = {
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%(APF|DOT1X)-({priority}\d+)-({event_name}[^:]+):\s\w+\.c:({event_code}\d+)"""
  
}
```