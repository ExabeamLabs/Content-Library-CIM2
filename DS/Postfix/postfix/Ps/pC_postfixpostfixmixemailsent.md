#### Parser Content
```Java
{
Name = postfix-postfix-mix-email-sent
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
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
    """\Wto=<?(\\u\d+)?((({dest_user}[\w\-\.]+)@localhost)|(({=dest_user}[^@>]+?)@({dest_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|>]+)))""",
    """\Wrelay=({dest_host}[\w\-.]+)\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """originalAgentHostName =({host}[^"]+)\soriginalAgentAddress"""
    """\Wstatus=({result}\w+)"""
    """Hostname=({host}[\w\-.]+)""",
    """\s({bytes}\d+)\s+bytes in """
  ]


}
```