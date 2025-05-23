#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-email-send-success-smtp
  Vendor = Forcepoint
  Product = Forcepoint DLP
  TimeFormat = ["epoch", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """|Forcepoint|Forcepoint DLP|""", """sourceServiceName =""", """sourceServiceName =SMTP""" ]
  Fields = [
    """timeStamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """\Wrt=({time}\d{13})""",
    """\Wdvc=(N\/A|({host}[A-Fa-f:\d.]+))""",
    """\Wdvchost=(N\/A|({host}[\w\-.]+))""",
    """({host}[\w\-.]+)\s+CEF:""",
    """\Wact=({result}.+?)(\s\-\s|\s+[\w\.]+=|$)""",
    """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wfname=\s*({email_attachment}[^;]+?)(;.*?)?\s*([\w\.]+=|$)""",
    """\Wfname=({file_name}[^-]*(\.({file_ext}\w+)))(N\/A|.*? - ({bytes}\d+\.?\d*)\s*({bytes_unit}[^\s;]+))"""
    """\Wfname=\s*(N\/A|-|({email_attachments}({email_attachment}[^=;]+)[^=]*))\s([\w\.]+=|$)"""
    """\Wmsg=\s*({email_subject}.+?)(\s+\-\s|\s+[\w\.]+=|$)""",
    """\Wcat=({alert_name}.+?)(\s\-\s|\s+[\w\.]+=|$)""",
    """\WsourceServiceName =({alert_type}.+?)\s+(on |\w+=)""",
    """\WloginName =(?:N\/A|(({domain}[^\\,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s\-\s|\s+[\w\.]+=|$)""",
    """\WsourceIp=(?:N\/A|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\WseverityType=({alert_severity}[^\s]+)""",
    """\WsourceHost=(?:N\/A|({src_host}[\w\-.]+))""",
    """\WdestinationHosts=(?:N\/A|(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+)))""",
    """\Wsuser=(({domain}[^\\\s,@=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\Wsuser=(Executive Inquiry Mailbox|({full_name}[^\\\s,@=]+?\s+[^\\,@=]+?))\s+(\w+=|$)""",
    """\Wsuser=({last_name}[^\\,=]+?),\s+({first_name}[^\\,=]+?)\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^\\\s,@=]+?@[^\\\s,@=]+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "email_attachments->attachment"]
  ParserVersion = "v1.0.0"


}
```