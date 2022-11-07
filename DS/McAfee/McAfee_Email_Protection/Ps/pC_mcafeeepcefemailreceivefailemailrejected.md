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
    """\Wrt=({time}\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wact=({action}.+?)\s+([\w\\]+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WFrom\\=<({email_address}[^\s>]+)""",
    """\Wsize=(|({bytes}\d+))""",
    """\Wto\\=<(unknown|({email_recipients}[^>]+))""",
    """\Wto\\=<(unknown|({email_recipients}[^\s>,;]+))""",
    """\Wattachment\(s\)\\='(|({email_attachments}[^']+))'""",
    """\Wattachment\(s\)\\='(|({email_attachments}[^,']+)),""",
  ]
  DupFields = [ "alert_name->alert_type" ]
  ParserVersion = "v1.0.0"


}
```