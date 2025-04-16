#### Parser Content
```Java
{
Name = cisco-ise-str-app-notification-alarm
  Conditions = [ """CISE_Alarm""", """ise2-""" ]
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """CISE_Alarm ({event_category}[^:]+):\s*({event_name}.+?)\s*:""",
# nas_identifier is removed
    """Server=({src_host}.+?)(?:;|$)""",
    """NAS IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:;|$)""",
    """Details=({additional_info}.+?)(?:;|$)""",
    """Failure Reason=({failure_reason}[^\s]+)\s"""
  ]


}
```