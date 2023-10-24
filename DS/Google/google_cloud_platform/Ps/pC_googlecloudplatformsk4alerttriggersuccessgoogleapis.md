#### Parser Content
```Java
{
Name = google-cloudplatform-sk4-alert-trigger-success-googleapis
  Vendor = Google
  Product = Google Cloud Platform 
  TimeFormat = "epoch"
  Conditions = [ """"type":"ids.googleapis.com""", """"type":"vulnerability"""", """"source_ip_address":""", """"alert_severity":""" ]
  Fields = [
    """"timestamp":({time}\d{13})\,""",
    """"source_ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"source_port":"({src_port}\d+)"""",
    """"destination_ip_address":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
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