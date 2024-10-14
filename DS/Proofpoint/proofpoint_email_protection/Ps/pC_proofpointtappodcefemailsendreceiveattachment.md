#### Parser Content
```Java
{
Name = proofpoint-tappod-cef-email-send-receive-attachment
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "MMM dd HH:mm:ss"]
  Conditions = [
"""mod=mail cmd=attachment"""
  ]
  Fields = [
    """"+host"+:"+({host}[^"]+)""",
    """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+[-+]\d+:\d+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"+"""
    """\sx=({alert_id}.+?)\s+(\w+=|$)""",
    """\sfile="*({email_attachment}[^=]+?)"*\s+(\w+=|$)""",
    """\sa=({attachment_count}\d+)""",
    """\sfile="*[^=]+(\.({file_ext}[^=]+?))"*\s+(\w+=|$)""",
    """\ssha256=({hash_sha256}[^=]+?)\s+\w+="""
  ]


}
```