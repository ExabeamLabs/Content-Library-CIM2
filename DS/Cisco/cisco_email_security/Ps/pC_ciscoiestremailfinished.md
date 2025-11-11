#### Parser Content
```Java
{
Name = cisco-ie-str-email-finished
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
    Conditions = [ """Message finished MID """ ]
    Fields = [
      """({time}\w+ \d\d \d\d:\d\d:\d\d)\s+"""
      """\srt=({time}\d+)""",
      """Message finished MID ({message_id}({alert_id}\d+)) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)"""
    ]
  

}
```