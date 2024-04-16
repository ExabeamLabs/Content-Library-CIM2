#### Parser Content
```Java
{
Name = symantec-esc-str-email-delivery
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|DELIVER"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|(|({action}[^\|]+))\|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}:\d+\|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|(|({action}[^\|]+))\|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}:\d+\|(|({failure_reason}[^\|]+))\|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    ]
  

}
```