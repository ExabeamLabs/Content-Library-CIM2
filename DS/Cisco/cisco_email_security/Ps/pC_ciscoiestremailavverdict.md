#### Parser Content
```Java
{
Name = cisco-ie-str-email-av-verdict
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """ AV verdict """ ]
    Fields = [
      """\srt=({time}\d+)""",
      """\d\d:\d\d:\d\d\s*({host}[\w\-\.]+)\s*""",
      """MID ({alert_id}\d+)""",
      """AV verdict using\s.+?\s({malware_score}[^\s"]+)""",
     ]
    DupFields = [ "alert_id->message_id" ]
  

}
```