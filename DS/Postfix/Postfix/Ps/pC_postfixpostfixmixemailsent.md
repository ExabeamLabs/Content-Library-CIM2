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
    """\Wrt=({time}\d+)""",
    """({message_id}[^\s"]+): to=<""",
    """"host(_name)?":"({host}[^"]+)""",
    """\d\d:\d\d:\d\d ({host}\S+) ( postfix[^:]+: )?""",
    """\Wto=<({email_recipients}[^\>]+)""",
    """\Wto=<({dest_email_address}[^\s\>,;]+)""",
    """\Wrelay=({dest_host}[\w\-.]+)\[({dest_ip}[a-fA-F:\d.]+)""",
    """originalAgentHostName =({host}[^"]+)\soriginalAgentAddress"""
  ]


}
```