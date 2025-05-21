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
      """\Wdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """suid=([^:\s]+:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """({app}Alliance Web Platform)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """msg=({additional_info}[^=]+?)\.?(\s*\w+=|\s*$)"""
    ]
  ParserVersion = "v1.0.0"


}
```