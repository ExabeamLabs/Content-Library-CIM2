#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-selinux
    Vendor = Unix
    Product = Unix
    TimeFormat = "MMM dd HH:mm:ss"
    Conditions = [ """ setroubleshoot[""", """]: SELinux is preventing""" ]
    Fields = [
      """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s""",
      """({event_name}setroubleshoot)""",
      """\]:\s+({additional_info}SELinux\s[^"$]+)"""
    ]
    ParserVersion = "v1.0.0"
  

}
```