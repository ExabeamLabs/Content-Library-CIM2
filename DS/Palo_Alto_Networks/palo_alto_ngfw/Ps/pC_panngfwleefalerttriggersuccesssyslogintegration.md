#### Parser Content
```Java
{
Name = pan-ngfw-leef-alert-trigger-success-syslogintegration
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [ """LEEF:""", """|Palo Alto Networks|PAN-OS Syslog Integration|""" ,"""|Severity="""]
  Fields = [
    """Severity=({alert_severity}[^\s|]+)""",
    """DeviceName =({host}[\w\-.]+)""",
    """LEEF:([^|]*\|){4}({alert_name}[^\|]+)""",
    """Subtype=({alert_type}[^\s\|]+)\s*\|""",
    """devTime=({time}[^\|]+)\s*\|""",
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """msg="({additional_info}[^"]+)"""",
    """sequence=({alert_id}\d+)""",
    """msg="(C|c)lient\s'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```