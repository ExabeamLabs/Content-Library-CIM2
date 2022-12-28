#### Parser Content
```Java
{
Name = symantec-esc-str-email-accept
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|ACCEPT|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ACCEPT\|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)"""
    ]
  

}
```