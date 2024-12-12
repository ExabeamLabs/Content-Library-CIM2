#### Parser Content
```Java
{
Name = cisco-ie-str-email-url-1
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ssz"]
    Conditions = [ """MID """, """URL Reputation Rule""" ]
    Fields = [
      """\d\d:\d\d\s+({host}[^\s]+)\s*""",
      """\srt=({time}\d+)""",
      """({time}\w+ \d+ \d\d:\d\d:\d\d) mail_logs:""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+[\d\:]+)""",
      """MID ({alert_id}\d+)""",
      """URL ({url}.+?) has reputation ({spam_score}.+?) matched Condition: URL Reputation Rule""",
     ]
    DupFields = [ "alert_id->message_id" ]
  

}
```