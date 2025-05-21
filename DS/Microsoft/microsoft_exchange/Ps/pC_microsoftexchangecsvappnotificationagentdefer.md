#### Parser Content
```Java
{
Name = microsoft-exchange-csv-app-notification-agentdefer
  ParserVersion = v1.0.0
  Conditions = [ """,AGENT,DEFER,""" ]

exchange-dlp-email-alert-2 = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """([^,]*,){1}\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*,""",
    """([^,]*,){2}\s*({src_host}[\w\-.]+)\s*,""",
    """([^,]*,){3}\s*(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s*,""",
    """([^,]*,){4}\s*({dest_host}[\w\-.]+)\s*,""",
    """,({log_source}SMTP|AGENT|ROUTING|DSN)""",
    """,({event_code}HADISCARD|HARECEIVE|AGENTINFO|RECEIVE|HAREDIRECT|SEND|SUPPRESSED|RESOLVE|TRANSFER|BADMAIL|EXPAND|DROP|DSN|REDIRECT)""",
    """,(SMTP|AGENT|ROUTING|DSN),[A-Z]+,([^,]*,){3}[\s<]*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,>]*?)(?<!local)(?<!loc)(?<!localdomain)(?<!internal)[\s>]*,""",
    """,\s*({email_subject}[^,]+?)["\s]*,([^,]*,){3}(Incoming|Originating),""",
    """,\s*"({email_subject}[^"]+?)\s*",([^,]*,){3}(Incoming|Originating),""",
    """,[<\s]*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?<!local)(?<!loc)(?<!localdomain)(?<!localhost)[\s>]*,([^,]*,){2}({direction}Incoming|Originating),""",
    """[\s>]*,([^,]*,){2}({direction}Incoming|Originating),""",
# transport_traffic_type is removed
  
}
```