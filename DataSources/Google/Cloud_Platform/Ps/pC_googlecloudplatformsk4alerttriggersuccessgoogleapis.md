#### Parser Content
```Java
{
Name = google-cloudplatform-sk4-alert-trigger-success-googleapis
  Vendor = Google
  Product = Cloud Platform 
  TimeFormat = "epoch"
  Conditions = [ """ destinationServiceName =Google Cloud Platform (GCP) """, """"type":"ids.googleapis.com""", """"type":"vulnerability"""", """"source_ip_address":""", """"alert_severity":""" ]
  Fields = [
    """"timestamp":({time}\d+)\,""",
    """"source_ip_address":"({src_ip}[A-Fa-f\d\.:]+)"""",
    """"source_port":"({src_port}\d+)"""",
    """"destination_ip_address":"({dest_ip}[A-Fa-f\d\.:]+)"""",
    """"destination_port":"({dest_port}\d+)"""",
    """"name":"({alert_name}[^"]+)"""",
    """"type":"({alert_type}vulnerability)"""",
    """"alert_severity":"({alert_severity}[^"]+)"""",
    """"ip_protocol":"({protocol}[^"]+)"""",
    """"details":"({additional_info}[^"]+)"""",
    """"threat_id":"({alert_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```