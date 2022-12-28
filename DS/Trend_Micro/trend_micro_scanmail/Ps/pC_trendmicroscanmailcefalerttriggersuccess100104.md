#### Parser Content
```Java
{
Name = trendmicro-scanmail-cef-alert-trigger-success-100104
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Trend Micro ScanMail
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Trend Micro|SMEX|""", """|100104|Web Threat Detection|""" ]
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d-\d\d:\d\d\s+({host}[^\s]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^|]+)""",
    """CEF:([^\|]*\|){5}({alert_type}[^|]+)""",
    """CEF:([^\|]*\|){4}({event_code}[^|]+)""",
    """cat=((?i)Unknown|({alert_type}[^=,]+))(\s+,\S+)?\s+\w+=""",
    """duser=({email_recipients}({dest_email_address}[^;]+)[^=]+?);?\s+\w+=""",
    """suser=({email_address}[^\s;]+);?\s+\w+=""",
    """act=({action}[^\s=])\s+\w+=""",
    """policyReason=({malware_url}[^\s]+)""",
    """msg=({additional_info}[^=]+)\s+\w+="""
    ]
  DupFields = [ "additional_info->alert_subject" ]


}
```