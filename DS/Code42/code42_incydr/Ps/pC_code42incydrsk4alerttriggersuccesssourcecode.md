#### Parser Content
```Java
{
Name = code42-incydr-sk4-alert-trigger-success-sourcecode
  Vendor = Code42
  Product = Code42 Incydr
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions= [ """"actor": """", """"OBSERVATION"""", """Source Code to External Destinations""" ]
  Fields = [
    """"observedAt":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"ALERT_DETAILS"[^\}]+?"name":\s*"({alert_name}[^"]+)",\s*"description":\s*"({additional_info}[^,]+)",\s*"actor":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"ALERT_DETAILS"[^\}]+?"id":\s*"({alert_id}[^"]+)"""",
    """"severity":\s*"({alert_severity}[^",]+)""",
    """"OBSERVATION"[^\}]+?"type":\s*"({alert_type}[^"]+)"""",
    """"OBSERVED_FILE"[^\}]+?"path":\s*"({file_dir}[^"]+)",\s*"name":\s*"({file_name}[^"]+)",\s*"category":\s*"({file_type}[^"]+)",\s*"size":\s*({bytes}\d+?),"""
    """"sendingIpAddresses":\s*\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]


}
```