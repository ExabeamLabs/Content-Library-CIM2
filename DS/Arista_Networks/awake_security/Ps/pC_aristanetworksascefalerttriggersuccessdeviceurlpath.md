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
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\s+""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))\s+""",
    """shost=({src_host}[^=]+)\s+(\w+=|$)""",
    """cs3=({os}[^=]+)\s+cs3Label=""",
    """cs2=({additional_info}[^\n]+)\s+cs2Label=""",
    """CEF:([^\|]*\|){4}({alert_id}[^\|]+)\|"""
  ]


}
```