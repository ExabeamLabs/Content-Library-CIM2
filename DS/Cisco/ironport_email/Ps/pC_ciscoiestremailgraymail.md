#### Parser Content
```Java
{
Name = cisco-ie-str-email-graymail
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """ , """GRAYMAIL """ ]
    Fields = [
      """\srt=({time}\d+)""",
      """\d\d:\d\d:\d\d\s*({host}[\w\-\.]+)\s*""",
      """MID ({alert_id}\d+)""",
      """GRAYMAIL\s({graymail_score}[^\s"]+)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```