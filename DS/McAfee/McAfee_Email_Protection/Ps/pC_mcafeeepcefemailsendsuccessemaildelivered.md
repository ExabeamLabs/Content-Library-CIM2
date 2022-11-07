#### Parser Content
```Java
{
Name = mcafee-ep-cef-email-send-success-emaildelivered
  Vendor = McAfee
  Product = McAfee Email Protection
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|Secure Internet Gateway|""", """|smtp:Email Delivered|""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({alert_name}[^\|]+)""",
    """\Wrt=({time}\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wact=({result}.+?)\s+([\w\\]+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WFrom\\=<({email_address}[^\s>]+)""",
    """\Wsize=({bytes}\d+)""",
    """\Wto\\=<({email_recipients}[^>]+)""",
    """\Wto\\=<({email_recipient}[^\s>,;]+)""",
    """\Wsubject\\='({email_subject}[^']+)""",
    """\Wattachment\(s\)\\='(|({email_attachments}[^']+))'""",
    """\Wattachment\(s\)\\='(|({email_attachment}[^,']+)),""",
    """\Wnumber-attachment\(s\)='({num_attachments}\d+)""",
  ]
  DupFields = [ "alert_name->alert_type" ]
  ParserVersion = "v1.0.0"


}
```