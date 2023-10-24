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
    """\('from',\s*'(({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))'\)""",
    """\('from',\s*'.*?<(({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))>'\)""",
    """\('to',\s*'({email_recipients}.*?)'\)""",
    """\('to',\s*'.*?<({email_recipients}.*?)>'\)""",
    """\('to',\s*'[\<]?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|'\)]+))""",
    """\('to',\s*'[\"][^\<]+[\<]?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|'\)>]+))""",
    """\('to',\s*'({external_address}[^@<>]+@[^>,<']+).*?'\)""",
    """\('to',\s*'.*?<({external_address}[^@><]+@[^>,<']+).*?'\)""",
    """\('(subject|Subject)',\s*'({email_subject}.*?)'\)""",
    """\('(x-fr({direction}o)m-mailhub|X-Fr({=direction}o)m-MailHub)',\s*'true'\)"""
  ]
  DupFields = [ "user->src_email_address" ]


}
```