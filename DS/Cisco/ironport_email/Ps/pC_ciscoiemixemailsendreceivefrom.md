#### Parser Content
```Java
{
Name = cisco-ie-mix-email-send-receive-from
    Vendor = Cisco
    Product = IronPort Email
	  ParserVersion = v1.0.0
    TimeFormat = "epoch"
    Conditions = [ """MID """, """CID """, """From""" ]
    Fields = [
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """(F|f)rom[:'].+?<({src_email_address}[^@>]+@[^>]+)>"""
    ]
  

}
```