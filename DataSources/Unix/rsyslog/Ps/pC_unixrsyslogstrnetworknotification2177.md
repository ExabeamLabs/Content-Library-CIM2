#### Parser Content
```Java
{
Name = unix-rsyslog-str-network-notification-2177
  ParserVersion = "v1.0.0"
  Vendor = Unix
  Product = rsyslog
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ rsyslogd-2177:""", """ imuxsock""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+)? rsyslogd-2177:""",
    """\srsyslogd-2177:\s*({additional_info}.+?)\s*$"""
  ]


}
```