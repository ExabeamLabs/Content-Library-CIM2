#### Parser Content
```Java
{
Name = unix-sm-kv-email-envelopesender
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
""" displayname=""",
""" connectingip=""",
""" envelopesender="""
  ]
  Fields = [
    """\d{2}:\d{2}:\d{2} ({host}[\w.\-]+)""",
    """\sqid="({alert_id}[^"]+)""",
    """\srecipients="({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\ssubject="({email_subject}.+?)"(,\s|\s*$)""",
    """\smsg_direction=({direction}[^,]+)"""
  ]


}
```