#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-success-chroot
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """sshd-chroot[""" ]
  Fields = [
    """\w{3}\s*\d\s\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)\s({event_code}[^:\s]+)\s*:?\s*({event_name}.+?)\sfrom\s({src_ip}[A-Fa-f:\d.]+)(\s*port\s*({src_port}\d+))?""",
    """\w{3}\s*\d\s\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)\s({event_code}[^:\s]+)\s*:?\s*({event_name}.+?)\sfor.+?\[({src_ip}[A-Fa-f:\d.]+)\]\s({alert_name}.+?)\s*$""",
]


}
```