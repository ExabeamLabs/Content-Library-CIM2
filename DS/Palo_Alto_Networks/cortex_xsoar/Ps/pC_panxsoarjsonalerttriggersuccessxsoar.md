#### Parser Content
```Java
{
Name = pan-xsoar-json-alert-trigger-success-xsoar
  Vendor = Palo Alto Networks
  Product = Cortex XSOAR
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"severity":"""", """"snowNumber"""", """"id":"XSOAR""" ]
  Fields = [
    """"username":\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """"type":\s*"({alert_type}[^"]+)"""",
    """"platform":\s*"({alert_source}[^"]+)"""",
    """"id":\s*"({alert_id}[^"]+)"""",
    """"name":\s*"({alert_name}[^"]+)"""",
    """"createdOn":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,9}Z""",
    """"severity":\s*"({alert_severity}[^"]+)"""",
    """"hostname":\s*"({host}[\w\-.]+)"""",
    """"sourceIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```