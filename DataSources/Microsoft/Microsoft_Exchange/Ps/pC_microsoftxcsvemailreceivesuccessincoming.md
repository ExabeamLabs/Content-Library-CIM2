#### Parser Content
```Java
{
Name = microsoft-x-csv-email-receive-success-incoming
  Vendor = Microsoft
  Product = Microsoft Exchange
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:m:ss.SSS"
  Conditions = [ 
""",SMTP,SEND,""" 
""",Incoming,""" 
]
  Fields = [
    """,({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+)""",
    """\d+:\d+\.\d+Z,[A-Fa-f:\d.]+,({host}[\w\.\-]+),""",
    """({additional_info}SMTP),({action}[^,]+),({alert_id}\d+),""",
    """({direction}Incoming)""",
    """,({email_recipients}({dest_email_address}[^\s@;,"]+@[^\s@;,"]+)[^,]*?),(?:[^",]+?,|,)({bytes}\d+),({num_recipients}\d+),(?:"(?:[^"]|"")+",|[^",]+?,|,){6}Incoming,""",
    """,\s*({email_subject}[^,]*?)\s*,(?:[^",]+?,|,){3}Incoming,""",
    ""","\s*({email_subject}[^"]+?)\s*",(?:[^",]+?,|,){3}Incoming,""",
    """,(MicrosoftExchange[^,]+?|({email_address}[^\s,;@"']+@[^\s;,"'@]+)),(?:<>|({return_path}[^,]+?)),(?:[^",]+?,|,)Incoming,"""
  ]


}
```