#### Parser Content
```Java
{
Name = aristanetworks-as-cef-alert-trigger-success-deviceurlpath
  ParserVersion = v1.0.0
  Vendor = Arista Networks
  Product = Awake Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """awakesecurity""", """|Arista Networks|Awake Security|""", """DeviceUrlPath""" ]
  Fields = [
    """deviceCustomDate1=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """CEF:([^\|]*\|){5}({alert_type}[^:\(]+)?\:?""",
    """CEF:([^\|]*\|){5}[^:\(]*[:\s]*({alert_name}[^\|]+?)(\s\([^\)]+\))?\|""",
    """CEF:([^\|]*\|){6}({alert_severity}\d+)\|""",
    """src=({src_ip}[A-Fa-f\d:\.]+)\s+""",
    """dst=({dest_ip}[A-Fa-f\d:\.]+)\s+""",
    """shost=({src_host}[^=]+)\s+(\w+=|$)""",
    """cs3=({os}[^=]+)\s+cs3Label=""",
    """cs2=({additional_info}[^\n]+)\s+cs2Label=""",
    """CEF:([^\|]*\|){4}({alert_id}[^\|]+)\|"""
  ]


}
```