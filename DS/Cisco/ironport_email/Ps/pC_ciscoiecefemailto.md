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
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+) .*? To: <({dest_email_address}[^@>,;]+?@[^>,;]+)>""",
      """ To: <({email_recipients}[^>]+?)>""",
      """\ssuser=\s*({email_address}[^\@\]\s"\\,\|]+\@[^\s]+\.[^\]\s"\\,\|]+)\s*""",
      """cs6=({email_subject}[^=]+)\s+""",
      """\sagt=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*"""
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```