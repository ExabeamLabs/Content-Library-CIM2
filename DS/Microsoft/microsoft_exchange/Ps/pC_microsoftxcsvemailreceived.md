#### Parser Content
```Java
{
Name = microsoft-x-csv-email-received
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""",Originating,"""
""",STOREDRIVER,""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)Z,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){6}STOREDRIVER,""",
    """,({host}[^\s,]+),(?:(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|,){3}STOREDRIVER,""",
    """,[^\s,]+:({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){3}STOREDRIVER,""",
    """,\s*(?:'|")?({host}[\w\.-]+)(?:'|")?\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}STOREDRIVER,""",
    """({additional_info}STOREDRIVER,({action}[^,]+)),""",
    """({direction}Originating)""",
    """,STOREDRIVER,[^,]+,\s*({alert_id}\d+)\s*,""",
    """,\s*({email_subject}[^,]+?)\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){3}Originating,""",
    """,\s*'({email_subject}(?:[^']|'')+)'\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){3}Originating,""",
    """,\s*"({email_subject}(?:[^"]|"")+?)\s*"\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){3}Originating,""",
    """,\s*(?:'|")?(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:'|")?)\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Originating,""",
    """,\s*(?:'|")?(?:<>|({return_path}[^,]+?))(?:'|")?\s*,(?:(?:\s*'+[^']*'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,)Originating,""",
    """,\s*(?:'|")?(([^,]+Recipients_cn\=)?({email_recipients}[^,]+?))\s*(?:'|")?,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){9}Originating,""",
    """,\s*(?:'|")?([^,]+Recipients_cn\=)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(?:'|")?,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){9}Originating,""",
    """,\s*({bytes}\d+)\s*,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){7}Originating,""",
    """,\s*({num_recipients}\d+)\s*,(?:(?:\s*'(?:[^']|'')+')\s*,|(?:\s*"(?:[^"]|"")+")\s*,|[^",]+?,|\s*,){6}Originating,"""
]
DupFields = [ "email_address->orig_user" ]


}
```