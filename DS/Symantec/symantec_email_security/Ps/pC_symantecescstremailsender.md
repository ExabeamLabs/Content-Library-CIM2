#### Parser Content
```Java
{
Name = symantec-esc-str-email-sender
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|SENDER|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SENDER\|(?:<>|({email_address}[a-zA-Z0-9+_.-]+@[a-zA-Z0-9.-]+))"""
    ]
  

}
```