#### Parser Content
```Java
{
Name = unix-rsyslog-str-network-notification-2177
  ParserVersion = "v1.0.0"
  Vendor = Unix
  Product = rsyslog
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """ rsyslogd-2177:""", """ imuxsock""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\d\d:\d\d:\d\d ({host}\S+)? rsyslogd-2177:""",
    """\srsyslogd-2177:\s*({additional_info}.+?)\s*$"""
  ]


}
```