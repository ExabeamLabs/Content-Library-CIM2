#### Parser Content
```Java
{
Name = swift-s-cef-app-login-fail-loginfailure
  ParserVersion = v1.0.0
  Product = Swift
  Conditions = [ """|SWIFT|Alliance Web Platform|""", """|login.failure|"""]
  Fields = ${SwiftAllianceWebPlatformTemplates.Swift-Alliance-Web-Platform.Fields}[
    """Message:\s*({failure_reason}[^:]+?)\.?(?:\\n)?Severity:"""
  ]

Swift-Alliance-Web-Platform = {
    Vendor = Swift
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
      """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[+-]\d\d:\d\d)\s\S+\s\S+\sCEF:""",
      """CEF:([^|]+\|){5}({event_name}[^|]+)\|({alert_severity}[^|]+)\|""",
      """\Wdvc=({dest_ip}[A-Fa-f:\d.]+)""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """suid=([^:\s]+:)?({user}[^\s]+)""",
      """({app}Alliance Web Platform)""",
      """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
      """msg=({additional_info}[^=]+?)\.?(\s*\w+=|\s*$)"""
    
}
```