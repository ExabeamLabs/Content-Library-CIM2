#### Parser Content
```Java
{
Name = cisco-ie-str-email-url
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ssz"]
    Conditions = [ """MID """, """Custom Log Entry:""", """URL""" ]
    Fields = [
      """\d\d:\d\d\s+({host}[^\s]+)\s*""",
      """\srt=({time}\d+)""",
      """({time}\w+ \d+ \d\d:\d\d:\d\d) mail_logs:""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+[\d\:]+)""",
      """MID ({alert_id}\d+)""",
      """Custom Log Entry:\s*({result}.+?)\s*URL""",
      ]
    DupFields = [ "alert_id->message_id" ]
  

}
```