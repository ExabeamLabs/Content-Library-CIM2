#### Parser Content
```Java
{
Name = microsoft-x-csv-email-receive-failed
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""",Incoming,""" 
""",FAIL,""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z,[^,]*,({host}[^,]+),([^,]*,){5}FAIL,""",
    """,\s*['"]*({host}[\w\.-]+)['"]*\s*,([^,]*,){2}\w+,FAIL,""",
    """({additional_info}\w+,FAIL),\s*(({alert_id}\d+)|)\s*,""",
    """({result}FAIL)""",
    """FAIL,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)""",
    """FAIL,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:'|")?({orig_user}[A-Za-z0-9!#$%&'+\/?=^_`~.-]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)""",
    """,\s*(({bytes}\d+)|)\s*,\s*(({num_recipients}\d+)|)\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){6}Incoming,""",
    """,\s*({email_subject}[^,]+?)\s*,([^,]*,){3}Incoming,""",
    """,\s*'({email_subject}(?:[^']|'')+?)\s*'\s*,([^,]*,){3}Incoming,""",
    """,\s*"({email_subject}(?:[^"]|"")+?)\s*"\s*,([^,]*,){3}Incoming,""",
    """,\s*(?:'|")?(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:'|")?)\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Incoming,""",
    """,\s*(?:'|")?(?:<>|({return_path}[^,]+?))(?:'|")?\s*,([^,]*,)Incoming,""",
    """({direction}Incoming)"""
    """RecipientNotFound;\s+({failure_reason}[^};]+)"""
]


}
```