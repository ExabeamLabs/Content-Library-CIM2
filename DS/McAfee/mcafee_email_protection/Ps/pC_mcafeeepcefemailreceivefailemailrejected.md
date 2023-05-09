#### Parser Content
```Java
{
Name = mcafee-ep-cef-email-receive-fail-emailrejected
  Vendor = McAfee
  Product = McAfee Email Protection
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|Secure Internet Gateway|""", """|smtp:Email Rejected|""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({alert_name}[^\|]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wact=({result}.+?)\s+([\w\\]+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WFrom\\=<({src_email_address}[^\s>]+)""",
    """\Wsize=(|({bytes}\d+))""",
    """\Wto\\=<(unknown|({email_recipients}[^>]+))""",
    """\Wto\\=<(unknown|({dest_email_address}[^\s>,;]+))""",
    """\Wattachment\(s\)\\='(|({email_attachments}[^']+))'""",
    """\Wattachment\(s\)\\='(|({email_attachment}[^,']+)),""",
  ]
  DupFields = [ "alert_name->alert_type" ]
  ParserVersion = "v1.0.0"


}
```