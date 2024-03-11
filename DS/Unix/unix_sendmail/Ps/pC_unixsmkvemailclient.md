#### Parser Content
```Java
{
Name = unix-sm-kv-email-client
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Sendmail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
""" msg_direction=""",
""" client_hostname=""",
""" client_ip="""
  ]
  Fields = [
    """\d{2}:\d{2}:\d{2} ({host}[\w.\-]+) \S+ \[.+?\-({alert_id}\w+)\]""",
    """\smsg_direction=({direction}[^,]+)""",
    """\sclient_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """client_hostname=({dest_host}[\w\-.]+),"""
  ]


}
```