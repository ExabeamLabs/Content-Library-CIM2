#### Parser Content
```Java
{
Name = postfix-postfix-kv-email-queue
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""postfix"""
"""from=<"""
"""nrcpt=""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)"""
    """({host}[\w.\-]+) postfix""",
    """({message_id}[^\s"]+): from=<?((root@host.company.web.ds)|(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))(?<!local)(?<!loc)(?<!localdomain)|({src_user}[^@>]+)@({src_domain}[^@>]+))>""",
    """\ssize=({bytes}\d+)""",
    """\snrcpt=({num_recipients}\d+)""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"host(_name)?":"({host}[^"]+)"""
    """\Wto=<({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]
  DupFields = [ "dest_email_address->email_recipients" ]


}
```