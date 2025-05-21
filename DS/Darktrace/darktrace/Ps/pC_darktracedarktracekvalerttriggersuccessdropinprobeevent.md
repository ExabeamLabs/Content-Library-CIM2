#### Parser Content
```Java
{
Name = darktrace-darktrace-kv-alert-trigger-success-dropinprobeevent
  Vendor = Darktrace
  Product = Darktrace
  TimeFormat = "epoch"
  Conditions = [ """darktrace""", """"Drop In Probe Events"""", """"status"""" ]
  Fields = [
    """"hostname"\s*:\s*"({host}[\w\-\.]+)"""",
    """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"priority":({priority}[^",]+)""",
    """"priority_level":"({alert_severity}[^"]+)"""",
    """"alert_name":"({alert_name}[^"]+)"""",
    """"status":"({alert_status}[^"]+)"""",
    """"message":"({additional_info}[^"]+)"""",
    """"uuid":"({user_uid}[^"]+)"""",
    """"url":"({url}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```