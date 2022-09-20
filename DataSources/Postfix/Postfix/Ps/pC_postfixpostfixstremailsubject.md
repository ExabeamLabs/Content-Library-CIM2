#### Parser Content
```Java
{
Name = postfix-postfix-str-email-subject
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""postfix"""
"""header Subject:""" 
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+) postfix[^:]+:\s*({message_id}[^\s:]+)""",
    """\WSubject:\s*({email_subject}[^;]+)""",
    """\Wfrom=<({email_address}[^\s\>]+)""",
    """\Wto=<({email_recipients}[^\>]+)""",
    """\Wto=<({dest_email_address}[^\s\>,;]+)""",
    """\Wfrom (unknown|({src_host}[\w\-.]+))\[({src_ip}[a-fA-F:\d.]+)"""
  ]


}
```