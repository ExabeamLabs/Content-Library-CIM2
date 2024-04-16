#### Parser Content
```Java
{
Name = postfix-postfix-str-email-subject
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss" ]
  Conditions = [ 
"""postfix"""
"""header Subject:""" 
]
  Fields = [
    """\s*({time}\w+\s*\d?\d\s\d+:\d+:\d+)""",
    """\d\d:\d\d:\d\d ({host}\S+) postfix[^:]+:\s*({message_id}[^\s:]+)""",
    """\WSubject:\s*({email_subject}[^;]+)""",
    """\Wfrom=<({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))""",
    """\Wto=<({email_recipients}[^\>]+)""",
    """\Wto=<({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))""",
    """\Wfrom (unknown|({src_host}[\w\-.]+))\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```