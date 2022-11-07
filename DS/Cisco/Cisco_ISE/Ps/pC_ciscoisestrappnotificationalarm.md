#### Parser Content
```Java
{
Name = cisco-ise-str-app-notification-alarm
  Conditions = [ """CISE_Alarm""", """ise2-""" ]
  Vendor = Cisco
  Product = Cisco ISE
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """CISE_Alarm ({event_category}[^:]+):\s*({event_name}.+?)\s*:""",
# nas_identifier is removed
    """Server=({src_host}.+?)(?:;|$)""",
    """NAS IP Address=({src_ip}.+?)(?:;|$)""",
    """Details=({additional_info}.+?)(?:;|$)""",
    """Failure Reason=({failure_reason}[^\s]+)\s"""
  ]


}
```