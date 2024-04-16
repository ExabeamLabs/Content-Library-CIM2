#### Parser Content
```Java
{
Name = cisco-ie-str-email-finished
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
    Conditions = [ """Message finished MID """ ]
    Fields = [
      """({time}\w+ \d\d \d\d:\d\d:\d\d)\s+"""
      """\srt=({time}\d+)""",
      """Message finished MID ({alert_id}\d+) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```