#### Parser Content
```Java
{
Name = postfix-postfix-mix-email-sent
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = epoch
  Conditions = [
"""postfix"""
"""dsn=2."""
"""status=sent""" 
]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """\Wrt=({time}\d{13})""",
    """({message_id}[^\s"]+): to=<""",
    """"host(_name)?":"({host}[^"]+)""",
    """\d\d:\d\d:\d\d ({host}\S+) ( postfix[^:]+: )?""",
    """\Wto=<({email_recipients}[^\>]+)""",
    """\Wto=<?(\\u\d+)?({dest_email_address}[^@>]+?@[^,\\>]+\.[^,\\>]+)>?""",
    """\Wrelay=({dest_host}[\w\-.]+)\[({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """originalAgentHostName =({host}[^"]+)\soriginalAgentAddress"""
  ]


}
```