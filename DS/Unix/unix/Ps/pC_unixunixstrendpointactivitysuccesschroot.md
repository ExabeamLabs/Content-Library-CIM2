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
    """\w{3}\s*\d\s\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)\s({event_code}[^:\s]+)\s*:?\s*({event_name}.+?)\sfrom\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\s*port\s*({src_port}\d+))?""",
    """\w{3}\s*\d\s\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)\s({event_code}[^:\s]+)\s*:?\s*({event_name}.+?)\sfor.+?\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s({alert_name}.+?)\s*$""",
]


}
```