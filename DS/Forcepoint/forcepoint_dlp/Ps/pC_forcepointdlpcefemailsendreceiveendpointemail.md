#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-email-send-receive-endpointemail
  Vendor = Forcepoint
  Product = Forcepoint DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """|Forcepoint|Forcepoint DLP|""", """act=""", """sourceServiceName =Endpoint Email""" ]
  Fields = [
    """timeStamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({host}[\w\-.]+)\s+CEF:""",
    """\Wact=({result}.+?)(\s\-\s|\s+[\w\.]+=|$)""",
    """\sduser=({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^;\]\s"\\,\|]+))[^=]+?)\s*\w+=""",
    """\Wfname=\s*(N\/A|-|({email_attachments}({email_attachment}[^=;]+)[^=]*))\s([\w\.]+=|$)"""
    """\Wmsg=\s*({email_subject}[^=]+)(\s+\-\s|\s+[\w\.]+=|$)""",
    """\WloginName =(?:N\/A|(({domain}[^\\,]+)\\+)?({user}[\w\.\-]{1,40}\$?))(\s\-\s|\s+[\w\.]+=|$)""",
    """\WsourceIp=(?:N\/A|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\WsourceHost=(?:N\/A|({src_host}[\w\-.]+))""",
    """\WdestinationHosts=(?:N\/A|(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+)))""",
    """\Wsuser=(({domain}[^\\\s,@=]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)""",
    """\Wsuser=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```