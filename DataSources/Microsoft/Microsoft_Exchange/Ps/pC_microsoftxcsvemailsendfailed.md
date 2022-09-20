#### Parser Content
```Java
{
Name = microsoft-x-csv-email-send-failed
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""",Originating,"""
""",FAIL,""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z,[^,]*,({host}[^,]+),([^,]*,){5}FAIL,""",
    """({additional_info}\w+,FAIL),""",
    """({action}FAIL)""",
    """,FAIL,\s*({alert_id}\d+)""",
    """,\s*(?:'|")?([^,]+Recipients_cn\=)?({email_recipients}({dest_email_address}[^,;'"\s@]+@[^,;'"\s@]+)[^,]*?)\s*(?:'|")?,([^,]*,){9}Originating,""",
    """,\s*(({bytes}\d+)|)\s*,\s*(({num_recipients}\d+)|)\s*,([^,]*,){6}Originating,""",
    """,\s*({email_subject}[^,]+?)\s*,([^,]*,){3}Originating,""",
    """,\s*'({email_subject}(?:[^']|'')+?)\s*'\s*,([^,]*,){3}Originating,""",
    """,\s*"({email_subject}(?:[^"]|"")+?)\s*"\s*,([^,]*,){3}Originating,""",
    """,\s*(?:'|")?(|MicrosoftExchange.*?|({email_address}[^,]+?)(?:'|")?)\s*,([^,]*,){2}Originating,""",
    """,\s*(?:'|")?(?:<>|({return_path}[^,]+?))(?:'|")?\s*,([^,]*,)Originating,"""
   ]
   DupFields = [ "email_address->orig_user" ]


}
```