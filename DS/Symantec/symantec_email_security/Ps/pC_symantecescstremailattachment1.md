#### Parser Content
```Java
{
Name = symantec-esc-str-email-attachment-1
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|ATTACH|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ATTACH\|({email_attachments}({email_attachment}.+?(\.({file_ext}.+?))?))"*\s*$"""
    ]
  

}
```