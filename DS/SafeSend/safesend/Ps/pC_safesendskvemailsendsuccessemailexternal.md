#### Parser Content
```Java
{
Name = safesend-s-kv-email-send-success-emailexternal
  Vendor = SafeSend
  Product = SafeSend
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """action=email_external""", """external_recipients="""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
    """\WComputerName =({host}[\w\-.]+)""",
    """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wfrom="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wsubject="({email_subject}[^"]+?)\s*"""",
    """\Wnr_total_recipients=({num_recipients}\d+)""",
    """\Wnr_internal_recipients=({num_internal_recipients}\d+)""",
    """\Wnr_external_recipients=({num_external_recipients}\d+)""",
    """\Wexternal_recipients="({email_recipients}[^"]*?<?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))[^"]*)"""",
    """\Wattachments="(|({email_attachments}[^"]+))""",
  ]
  ParserVersion = "v1.0.0"


}
```