#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-attachment
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint TAP/POD
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""mod=mail cmd=attachment"""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({xid}.+?)\s+(\w+=|$)""",
    """\sfile="*({email_attachment}[^=]+?)"*\s+(\w+=|$)""",
    """\sa=({attachment_count}\d+)""",
    """\sfile="*[^=]+(\.({file_ext}[^=]+?))"*\s+(\w+=|$)"""
  ]


}
```