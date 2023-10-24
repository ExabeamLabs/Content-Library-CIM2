#### Parser Content
```Java
{
Name = varonis-dsp-kv-alert-trigger-success-alerttriggerd
  Vendor = Varonis
  Product = Varonis Data Security Platform
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """| Varonis alert: ""","""| Alert details: """ ]
  Fields = [
    """\|\sEvent Time:\s({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s((?i)am|pm))""",
    """\|\sDevice hostname:\s(|({host}[^\|]+?))\s\|""",
    """\|\sActing Object:\s((Exchange Online|({domain}[^\\\|]+?))(\s\([^\)]+\))?\\+)?(S\-(\d+\-){6}\d+|other|({full_name}[^\|]+?))\s((\-|\()[^\|]+)?\|""",
    """\|\sActing Object SAM Account Name:\s(({user_sid}S\-(\d+\-){6}\d+)|({user}[\w\.\-]{1,40}\$?))\s\|""",
    """\|\sDevice IP address:\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\|""",
    """\|\sRule Name:\s({alert_name}[^\|]+?)\s\|""",
    """\|\sEvent Type:\s({alert_type}[^\|]+?)\s\|""",
    """\|\sSeverity:\s({alert_severity}\d{1,5})\s\|""",
    """\|\sRule ID:\s({alert_id}\d+)\s\|""",
    """\|\sEvent Status:\s({result}[^\|]+?)\s\|""",
    """\|\sRule Description:\s({additional_info}[^\|]+?)\s\|""",
    """\|\sPath:\s({additional_info}[^\|]+?)\s\|"""
  ]
  ParserVersion = "v1.0.0"


}
```