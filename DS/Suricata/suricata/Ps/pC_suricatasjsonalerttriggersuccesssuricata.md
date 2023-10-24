#### Parser Content
```Java
{
Name = suricata-s-json-alert-trigger-success-suricata
  Vendor = Suricata
  Product = Suricata
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"alert"""", """"event_source":"suricata"""", """"event_type":"alert""""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[\+\-]\d\d\d\d)""",
    """"signature":"({alert_name}[^"]+)""",
    """"severity":({alert_severity}\d)""",
    """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"event_type":"({alert_type}[^"]+)""",
    """"dest_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"dest_port":({dest_port}\d{1,5})""",
    """"src_port":({src_port}\d{1,5})""",
    """"signature_id":({alert_id}\d+)""",
    """"proto":"({protocol}\w+)""",
    """"payload":"({additional_info}[^"]+)""",
    """"sensor_hostname":"({src_host}[^"]+)"""
  ]


}
```