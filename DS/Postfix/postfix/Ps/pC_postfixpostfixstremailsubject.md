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
    """\Wfrom=<({sender}[^\s\>]+)""",
    """\Wto=<({email_recipients}[^\>]+)""",
    """\Wto=<({dest_email_address}[^\s\>,;]+)""",
    """\Wfrom (unknown|({src_host}[\w\-.]+))\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```