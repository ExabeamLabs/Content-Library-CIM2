#### Parser Content
```Java
{
Name = symantec-dlp-cef-alert-trigger-success-dlp
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "epoch"
  Conditions = [ """CEF""", """|Symantec|Symantec Data Loss Prevention|""" ]
  Fields = [
    """"collector_name":"({host}[^"]+)"""",
    """\Wrt=({time}\d+)""",
    """"desc":"({additional_info}[^"]+)"""",
    """"sender_ip":"({src_ip}[^"]+)"""",
    """"recipient_ip":"({dest_ip}[^"]+)"""",
    """"recipient_identifier":"({target}[^"]+)"""",
    """"policy":\{.*?"name":"({alert_name}[^"]+)"""",
    """"feature_name":"({alert_type}[^"]+)"""",
    """"event_id":({alert_id}\d+)""",
    """"severity_id":({alert_severity}\d+)""",
    """"product_name":"({product_name}[^"]+)"""",
  ]


}
```