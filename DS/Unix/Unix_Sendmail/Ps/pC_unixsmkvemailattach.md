#### Parser Content
```Java
{
Name = unix-sm-kv-email-attach
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
""" attach_name=""",
""" attach_type=""",
""" attach_filename="""
  ]
  Fields = [
    """\d{2}:\d{2}:\d{2} ({host}[\w.\-]+)""",
    """\smtaqid=({alert_id}[^,]+)""",
    """\sattach_filename="({email_attachment}[^"]+\.({file_ext}[^"]+))"""
  ]


}
```