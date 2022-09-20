#### Parser Content
```Java
{
Name = symantec-brightmail-str-email-recipient
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Brightmail
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