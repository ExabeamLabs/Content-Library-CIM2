#### Parser Content
```Java
{
Name = dg-ndlp-cef-email-send-success-sendmail
  ParserVersion = v1.0.0
  Vendor = Digital Guardian
  Product = Digital Guardian Network DLP
  TimeFormat = "epoch"
  Conditions = [ 
"""|Digital Guardian|Digital Guardian|"""
"""|Send Mail|""" 
]
  Fields = [
    """\srt=({time}\d{13})""",
    """({event_code}Send Mail)""",
    """\sshost=(([^\/\\=]+)[\/\\]+)?({host}[^=]+?)\s+(ad\.\S+=|\w+=|$)""",
    """\sad\.DG__EmailSender=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\sad\.DG__EmailRecipient=({email_recipients}[^\s@]+@[^\s@]+)""",
    """\sad\.DG__EmailSubject=({email_subject}.+?)\s+(ad\.\S+=|\w+=|$)""",
    """\ssuser=(({domain}[^\/\\=]+)[\/\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(ad\.\S+=|\w+=|$)""",
    """\sfname=\s*(?:message body|({email_attachment}[^=]+?))\s+(ad\.\S+=|\w+=|$)"""
  ]


}
```