#### Parser Content
```Java
{
Name = f5-afm-cef-alert-trigger-attack
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Advanced Firewall Manager
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""","""|F5|Advanced Firewall Module|""","""cs6=Attack""","""cs4Label=dos_mode""","""cs5Label=dos_src"""]
  Fields = [
    """rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host}[^\s]+)""",
    """dst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """dpt=({dest_port}\d+)""",
    """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """spt=({src_port}\d+)""",
    """act=(None|({action}[^\s]+))""",
    """CEF:[^|]+\|([^|]+\|){4}(\/[^|]+|({alert_name}[^|]+))""",
    """CEF:[^|]+\|([^|]+\|){4}({alert_name}\/[^=]+)\/""",
    """CEF:[^|]+\|([^|]+\|){5}({alert_severity}[^|]+)""",
# dos_source is removed
    """cn1=({attack_id}\d+)""",
# attack_status is removed
# dos_protection_mode is removed
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```