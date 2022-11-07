#### Parser Content
```Java
{
Name = symantec-brightmail-str-email-sender
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Brightmail
    TimeFormat = "epoch_sec"
    Conditions = [
"""|SENDER|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SENDER\|(?:<>|({email_address}[^\|@]+@[^@]+?))(\||\s*$)"""
    ]
  

}
```