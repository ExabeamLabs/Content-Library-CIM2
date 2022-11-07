#### Parser Content
```Java
{
Name = symantec-brightmail-str-email-bytes
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Brightmail
    TimeFormat = "epoch_sec"
    Conditions = [
"""|MSG_SIZE|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|MSG_SIZE\|({bytes}\d+)"""
    ]
  

}
```