#### Parser Content
```Java
{
Name = cisco-ie-cef-email-file-verdict
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """file reputation verdict""" ]
    Fields = [
      """\d\d:\d\d\s+({host}[^\s]+)\s*""",
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """file reputation verdict\s*:\s*(?:UNKNOWN|({file_verdict}[^,\s]+))"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```