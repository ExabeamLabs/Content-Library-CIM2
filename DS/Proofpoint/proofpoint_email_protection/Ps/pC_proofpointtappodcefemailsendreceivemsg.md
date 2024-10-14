#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-msg
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [
"""mod=mail cmd=msg"""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[-+]\d+:\d+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({alert_id}.+?)\s+(\w+=|$)""",
    """\saction=({action}[^=]+?)\s+(\w+=|$)""",
    """\srcpts=({num_recipients}\d+)""",
    """\sroutes=({routes}[^=]+?)\s+(\w+=|$)""",
    """\ssize=({bytes}\d+)""",
    """\ssubject=\\*"+({email_subject}[^"=]+?)\\*"*\s+(\w+=|$)""",
    """\svirusname=({alert_name}[^=]+?)\s+(\w+=|$)"""
  ]


}
```