#### Parser Content
```Java
{
Name = unix-unix-str-smtp-start-connectfrom
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """postfix/smtpd[""",""" connect from""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d\s(::ffff:)?(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))|({dest_host}[\w\-.]+))\s*(::ffff:)?({host}[^\s]+)?\s*postfix""",
    """\s*({additional_info}postfix.+?)\s*$""",
    """from\s[^\[]+\[({dest_ip}[A-Fa-f.\d]+)""",
    """src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```