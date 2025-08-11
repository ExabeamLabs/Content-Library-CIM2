#### Parser Content
```Java
{
Name = "libraesva-libraes-str-email-mailscanner-delivery"
  Vendor = "Libraesva"
  Product = "Libraesva Email Security"
  TimeFormat = ["MMM dd HH:mm:ss", "MMM d HH:mm:ss"]
  Conditions = [ """ MailScanner[""","""with subject""","""delivery of"""]
  Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)\s+({host}[^\s]+)\s"""
    """\smessage ({message_id}\S+)\s"""
    """]:\s({result}(?i)(Non-)?Delivery)\sof"""
    """\sfrom\s({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+.[^\]\s"\\,;\|]+)\sto"""
    """\sto ({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^:]*?)\swith subject"""
    """\Wwith subject ({email_subject}(.+)$)"""
  ]
  ParserVersion = "v1.0.0"


}
```