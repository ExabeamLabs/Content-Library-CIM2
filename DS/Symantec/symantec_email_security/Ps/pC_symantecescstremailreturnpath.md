#### Parser Content
```Java
{
Name = symantec-esc-str-email-returnpath
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|MSGID|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|MSGID\|\s*(|<?({return_path}.+?)>?)(\||\s*$)"""
    ]
  

}
```