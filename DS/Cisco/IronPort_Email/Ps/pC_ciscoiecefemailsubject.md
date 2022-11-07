#### Parser Content
```Java
{
Name = cisco-ie-cef-email-subject
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ Subject """ ]
    Fields = [
      """ahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d+)""",
      """MID ({alert_id}\d+) Subject '?({email_subject}[^']+?)\s*('|$)""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```