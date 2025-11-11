#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-fail-sshd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """sshd[""", """]: """, """error:""" ]
  Fields = [
    """\s*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
    """(\d\d:|(\+|-))\d\d:\d\d (::ffff:)?({host}[\w\-.]+)\s""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """\ssshd\[\d+\]:\s*error:\s*({failure_reason}.+?)\s*$""",
    """Authentication failure for (({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\sfrom\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```