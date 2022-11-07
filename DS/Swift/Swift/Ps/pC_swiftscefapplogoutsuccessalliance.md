#### Parser Content
```Java
{
Name = swift-s-cef-app-logout-success-alliance
    Vendor = Swift
    Product = Swift
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """|SWIFT|Alliance Web Platform|""", """|logout.success|"""]
    Fields = [
      """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[+-]\d\d:\d\d)\s\S+\s\S+\sCEF:""",
      """({event_name}logout.success)\|({alert_severity}[^|]+)\|""",
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