#### Parser Content
```Java
{
Name = cisco-ie-cef-email-graymail
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "epoch"
    Conditions = [ """CEF""", """MID """ , """GRAYMAIL """ ]
    Fields = [
      """\srt=({time}\d{13})""",
      """\d\d:\d\d:\d\d\s*({host}[\w\-\.]+)\s*""",
      """MID ({alert_id}\d+)""",
      """GRAYMAIL\s({graymail_score}[^\s"]+)"""
      """MID ({message_id}\d+)""",
    ]
  

}
```