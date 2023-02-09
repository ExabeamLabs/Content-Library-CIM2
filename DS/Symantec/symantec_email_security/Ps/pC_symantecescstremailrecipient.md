#### Parser Content
```Java
{
Name = symantec-esc-str-email-recipient
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|ORCPTS|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ORCPTS\|({email_recipients}({dest_email_address}[^\|\s]+).*?)\s*$"""
    ]
  

}
```