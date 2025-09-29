#### Parser Content
```Java
{
Name = unix-unix-str-smtp-close-lostconnection
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """postfix/smtpd[""" ,""" lost connection after""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d\s(::ffff:)?(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))|({dest_host}[\w\-.]+))\s*(::ffff:)?({host}[^\s]+)?\s*postfix""",
    """\s*({additional_info}postfix.+?)\s*$""",
    """from\s[^\[]+\[({dest_ip}[A-Fa-f.\d]+)"""
    """\s+.*\/({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```