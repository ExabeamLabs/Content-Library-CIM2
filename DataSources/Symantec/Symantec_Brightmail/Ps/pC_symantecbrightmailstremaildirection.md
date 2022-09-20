#### Parser Content
```Java
{
Name = symantec-brightmail-str-email-direction
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Brightmail
    TimeFormat = "epoch_sec"
    Conditions = [
"""|SOURCE|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SOURCE\|({direction}\w+)"""
    ]
  

}
```