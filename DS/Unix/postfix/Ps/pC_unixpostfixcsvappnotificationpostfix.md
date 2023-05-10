#### Parser Content
```Java
{
Name = unix-postfix-csv-app-notification-postfix
  Vendor = Unix
  Product = Postfix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """][""", """ postfix """, """to=<""", """, dsn=""", """, status=""" ]
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) postfix""",
    """({msg_id}[^:\s]+):\s+to=<""",
    """\Wto=<({recipients}({recipient}[^>@,;]+@([^>@,;]+))[^>]*?)>""", # external_domain_recipient is removed
    """\Wrelay=({dest_host}[\w\-.]+)(\[({dest_ip}[a-fA-F:\d.]+)\])?,""",
    """\Wstatus=({action}sent|bounced)""",
    """\Wstatus=bounced \(\s*({failure_reason}.+?)\s*\)"""
]


}
```