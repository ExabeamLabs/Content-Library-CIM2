#### Parser Content
```Java
{
Name = cisco-ie-str-email-file-verdict
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ssz"]
    Conditions = [ """MID """, """file reputation verdict""" ]
    Fields = [
      """\d\d:\d\d\s+({host}[^\s]+)\s*""",
      """\srt=({time}\d+)""",
      """({time}\w+ \d+ \d\d:\d\d:\d\d) mail_logs:""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+[\d\:]+)""",
      """MID ({alert_id}\d+)""",
      """file reputation verdict\s*:\s*(?:UNKNOWN|({file_verdict}[^,\s]+))"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```