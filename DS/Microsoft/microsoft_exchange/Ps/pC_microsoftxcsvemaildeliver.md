#### Parser Content
```Java
{
Name = microsoft-x-csv-email-deliver
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""",Incoming,"""
""",STOREDRIVER,""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){6}STOREDRIVER,""",
    """,\s*['"]*({host}[\w\.-]+)['"]*\s*,([^,]*,){2}STOREDRIVER,""",
    """({alert_name}STOREDRIVER,({action}[^,]+)),""",
    """({direction}Incoming)""",
    """,STOREDRIVER,[^,]+,\s*({alert_id}\d+)\s*,""",
    """,\s*['"]*({email_recipients}[^,;@]+@[^;,"']+?)\s*['"]*,(?:[^,]*,){9}Incoming,""",
    """,\s*['"]*({orig_user}[^,;@]+@[^;,"']+)\s*['"]*,([^,]*,){9}Incoming,""",
    """,\s*({bytes}\d+)\s*,(?:[^,]*,){7}Incoming,""",
    """,\s*({num_recipients}\d+)\s*,(?:[^,]*,){6}Incoming,""",
    """,\s*({email_subject}[^,]+?)\s*,(?:[^,]*,){3}Incoming,""",
    """,\s*['"]*(|MicrosoftExchange.*?|({sender}[^@,]+@[^\.]+\.[^,]+)['"]*)\s*,(?:[^,]*,){2}Incoming,""",
    """,\s*['"]*(|.+?@({external_domain}[^,]+?)['"]*)\s*,(?:[^,]*,){2}Incoming,""",
    """,\s*['"]*(?:<>|({return_path}[^,]+?))['"]*\s*,(?:[^,]*,)Incoming,"""
  ]
  DupFields = [ "alert_name->alert_type","orig_user->email_address","email_recipients->dest_email_address" ]


}
```