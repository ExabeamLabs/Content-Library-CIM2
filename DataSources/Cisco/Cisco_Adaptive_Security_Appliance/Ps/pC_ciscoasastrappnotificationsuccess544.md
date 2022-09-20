#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-544
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  Conditions = [ """%DOT1X-4-MAX_EAPOL_KEY_RETRANS""", """1x_ptsm.c:544""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-network-template.Fields} [
    """({additional_info}Max EAPOL-key M5 retransmissions exceeded for client ({src_mac}[a-fA-F\d:.]+))"""
  ]

cisco-network-template = {
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """%(APF|DOT1X)-({priority}\d+)-({event_name}[^:]+):\s\w+\.c:({event_code}\d+)"""
  
}
```