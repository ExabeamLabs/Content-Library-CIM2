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
    """"collector_name":"({host}[\w\-\.]+)"""",
    """\Wrt=({time}\d{13})""",
    """"desc":"({additional_info}[^"]+)"""",
    """"sender_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"recipient_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"recipient_identifier":"({target}[^"]+)"""",
    """"policy":\{.*?"name":"({alert_name}[^"]+)"""",
    """"feature_name":"({alert_type}[^"]+)"""",
    """"event_id":({alert_id}\d+)""",
    """"severity_id":({alert_severity}\d+)""",
    """"product_name":"({product_name}[^"]+)"""",
  ]


}
```