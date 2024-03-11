#### Parser Content
```Java
{
Name = microsoft-exchange-csv-app-notification-success-queueresubmit
  ParserVersion = "v1.0.0"
  Conditions = [ """,QUEUE,RESUBMIT,""" ]
  Fields = ${MicrosoftParsersTemplates.exchange-dlp-email-alert.Fields}[
   """,QUEUE,RESUBMIT,([^,]*,){3}({email_recipients}({dest_email_address}[^,;@]+@([^,;@]+)[^,]*?))""", #dl field removed
   """,QUEUE,RESUBMIT,([^,]*,){9}({email_subject}[^,]+)""",
   """,QUEUE,RESUBMIT,([^,]*,){10}({src_email_address}[^,@]+@([^,@]+))""" #dl field removed
  ]

exchange-dlp-email-alert = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """([^,]*,){1}\s*(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*,""",
    """([^,]*,){2}\s*({src_host}[\w\-.]+)\s*,""",
    """([^,]*,){3}\s*(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s*,""",
    """([^,]*,){4}\s*({dest_host}[\w\-.]+)\s*,""",
    """,({log_source}SMTP|AGENT|ROUTING|DSN)""",
    """,({event_code}HADISCARD|HARECEIVE|AGENTINFO|RECEIVE|HAREDIRECT|SEND|SUPPRESSED|RESOLVE|TRANSFER|BADMAIL|EXPAND|DROP|DSN|REDIRECT)""",
    """,(SMTP|AGENT|ROUTING|DSN),[A-Z]+,([^,]*,){3}[\s<]*({email_recipients}({dest_email_address}[^,;"\s@<]+@[^,;"\s@>]+)[^,>]*?)[\s>]*,""",
    """,\s*({email_subject}[^,]+?)["\s]*,([^,]*,){3}(Incoming|Originating),""",
    """,\s*"({email_subject}[^"]+?)\s*",([^,]*,){3}(Incoming|Originating),""",
    """,[<\s]*({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)[\s>]*,([^,]*,){2}({direction}Incoming|Originating),""",
# transport_traffic_type is removed
  
}
```