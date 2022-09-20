#### Parser Content
```Java
{
Name = symantec-brightmail-str-email-subject
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Brightmail
    TimeFormat = "epoch_sec"
    Conditions = [
"""|SUBJECT|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SUBJECT\|\s*(|({email_subject}.+?))(\||\s*$)"""
    ]
  

}
```