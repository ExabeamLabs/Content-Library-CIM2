#### Parser Content
```Java
{
Name = "darktrace-darktrace-json-alert-trigger-success-alertname"
  Product = "Darktrace"
  Vendor = "Darktrace"
  TimeFormat = "epoch_sec"
  Conditions = [ """"hostname":""", """"priority_level":""", """"alert_name":""", """"status":""" ]
  Fields = [
    """"hostname":\s*"({src_host}[\w.-]+)"""
    """"last_updated":\s*({time}\d{10})"""
    """"ip_address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"url":\s*"({url}[^"]+)"""
    """"alert_name":\s*"({alert_name}[^"]+)"""
    """"priority":({alert_severity}\d+)"""
    """"name":\s*"({alert_type}[^"]+)"""   
    """"message":\s*"({additional_info}[^"]+)"""
    """"status":"({alert_status}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```