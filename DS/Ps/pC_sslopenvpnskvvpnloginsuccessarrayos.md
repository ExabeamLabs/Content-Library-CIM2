#### Parser Content
```Java
{
Name = "sslopenvpn-s-kv-vpn-login-success-arrayos"
Conditions = [
"""id=ArrayOS"""
"""A new TCP tunnel has been established successfully"""
"""type=vpn"""
]
ParserVersion = "v1.0.0"

Swift-Alliance-Web-Platform = {
    Vendor = Swift
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
      """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[+-]\d\d:\d\d)\s\S+\s\S+\sCEF:""",
      """CEF:([^|]+\|){5}({event_name}[^|]+)\|({alert_severity}[^|]+)\|""",
      """\Wdvc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """suid=([^:\s]+:)?({user}[^\s]+)""",
      """({app}Alliance Web Platform)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """msg=({additional_info}[^=]+?)\.?(\s*\w+=|\s*$)"""
    
}
```