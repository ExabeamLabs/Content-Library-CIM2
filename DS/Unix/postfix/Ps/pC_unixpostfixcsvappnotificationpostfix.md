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
    """\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[""",
    """<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) postfix""",
    """({msg_id}[^:\s]+):\s+to=<""",
    """\Wto=<({recipients}({dest_email_address}[^>@,;]+@([^>@,;]+))[^>]*?)>""", # external_domain_recipient is removed
    """\Wrelay=({dest_host}[\w\-.]+)(\[({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\])?,""",
    """\Wstatus=({action}sent|bounced)""",
    """\Wstatus=bounced \(\s*({failure_reason}.+?)\s*\)"""
]


}
```