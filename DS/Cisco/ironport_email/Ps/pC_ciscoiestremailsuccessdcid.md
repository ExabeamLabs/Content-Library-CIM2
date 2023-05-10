#### Parser Content
```Java
{
Name = cisco-ie-str-email-success-dcid
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = IronPort Email
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """Message done DCID""", """'from'""", """'to'""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\W({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\-\d\d:\d\d)\s({host}[^\s]+)\s""",
    """\WMessage done DCID \d+ MID ({alert_id}\d+)\s""",
    """\('from',\s*'({user}.*?)'\)""",
    """\('from',\s*'.*?<({user}.*?)>'\)""",
    """\('to',\s*'({email_recipients}.*?)'\)""",
    """\('to',\s*'.*?<({email_recipients}.*?)>'\)""",
    """\('to',\s*'[\<]?({dest_email_address}[^>,\';]+)""",
    """\('to',\s*'[\"][^\<]+[\<]?({dest_email_address}[^>,\';]+)""",
    """\('to',\s*'({external_address}[^@<>]+@[^>,<']+).*?'\)""",
    """\('to',\s*'.*?<({external_address}[^@><]+@[^>,<']+).*?'\)""",
    """\('(subject|Subject)',\s*'({email_subject}.*?)'\)""",
    """\('(x-fr({direction}o)m-mailhub|X-Fr({=direction}o)m-MailHub)',\s*'true'\)"""
  ]
  DupFields = [ "user->sender" ]


}
```