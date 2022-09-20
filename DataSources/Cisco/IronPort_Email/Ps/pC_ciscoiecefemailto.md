#### Parser Content
```Java
{
Name = cisco-ie-cef-email-to
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ RID """, """ To: """ ]
    Fields = [
      """\sahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d+)""",
      """MID ({alert_id}\d+) .*? To: <({dest_email_address}[^@>,;]+?@[^>,;]+)>""",
      """ To: <({email_recipients}[^>]+?)>""",
      """\ssuser=({email_address}[^\@]+\@[^\s]+)\s*""",
      """cs6=({email_subject}[^=]+)\s+""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*"""
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```