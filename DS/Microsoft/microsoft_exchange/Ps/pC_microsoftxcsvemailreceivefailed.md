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
    """({action}FAIL)""",
    """,\s*(?:'|")?(|MicrosoftExchange.*?|({sender}[^,@]+?@({external_domain}[^,]+?))(?:'|")?)\s*,(?:[^,]*,){2}Incoming,""",
    """,\s*(?:'|")?({email_recipients}({dest_email_address}[^,;'"\s@]+@[^,;'"\s@]+)[^,]*?)\s*(?:'|")?,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,""",
    """,\s*(?:'|")?({orig_user}[^,;@]+@[^;,"']+)[^,]*?\s*(?:'|")?,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,""",
    """,\s*(({bytes}\d+)|)\s*,\s*(({num_recipients}\d+)|)\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){6}Incoming,""",
    """,\s*({email_subject}[^,]+?)\s*,([^,]*,){3}Incoming,""",
    """,\s*'({email_subject}(?:[^']|'')+?)\s*'\s*,([^,]*,){3}Incoming,""",
    """,\s*"({email_subject}(?:[^"]|"")+?)\s*"\s*,([^,]*,){3}Incoming,""",
    """,\s*(?:'|")?(|MicrosoftExchange.*?|({sender}[^,@]+?@[^,]+?)(?:'|")?)\s*,([^,]*,){2}Incoming,""",
    """,\s*(?:'|")?(?:<>|({return_path}[^,]+?))(?:'|")?\s*,([^,]*,)Incoming,""",
    """({direction}Incoming)"""
]
  DupFields = [ "orig_user->email_address" , "sender->external_address"]


}
```