#### Parser Content
```Java
{
Name = cisco-ie-cef-email-av-verdict
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF""", """MID """, """ AV verdict """ ]
    Fields = [
      """\srt=({time}\d{13})""",
      """\d\d:\d\d:\d\d\s*({host}[\w\-\.]+)\s*""",
      """MID ({alert_id}\d+)""",
      """AV verdict using\s.+?\s({malware_score}[^\s"]+)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```