#### Parser Content
```Java
{
Name = swift-s-cef-app-notification-webplatform
    Vendor = Swift
    Product = Swift
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """|SWIFT|Alliance Web Platform|""", """|session.stale|"""]
    Fields = [
      """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[+-]\d\d:\d\d)\s\S+\s\S+\sCEF:""",
      """({event_name}session.stale)\|({alert_severity}[^|]+)\|""",
      """\Wdvc=({dest_ip}[A-Fa-f:\d.]+)""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """suid=([^:\s]+:)?({user}[^\s]+)""",
      """({app}Alliance Web Platform)""",
      """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
      """msg=({additional_info}[^=]+?)\.?(\s*\w+=|\s*$)"""
    ]
  ParserVersion = "v1.0.0"


}
```