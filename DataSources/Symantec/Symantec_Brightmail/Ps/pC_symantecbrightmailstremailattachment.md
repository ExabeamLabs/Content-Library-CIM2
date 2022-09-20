#### Parser Content
```Java
{
Name = symantec-brightmail-str-email-attachment
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Brightmail
    TimeFormat = "epoch_sec"
    Conditions = [
"""|ATTACHFILTER|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ATTACHFILTER\|(|({email_attachment}.+?(\.({file_ext}.+?))?))(\||"*\s*$)"""
    ]
  

}
```