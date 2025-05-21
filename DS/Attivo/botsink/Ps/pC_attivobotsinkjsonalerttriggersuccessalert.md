#### Parser Content
```Java
{
Name = "attivo-botsink-json-alert-trigger-success-alert"
Vendor = "Attivo"
Product = "BOTsink"
TimeFormat = ["yyyy MMM dd HH:mm:ss zzz"]
Conditions = [ """"app":"BOTsink:"""", """"Alert":""", ""","subject":"""", """"severity"""" ]
Fields = [
  """"timestamp":"({time}[^"]+)""""                     
  """<(?:\d{1,3})>(?:\d{0,2}\s)?(?:\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2})\s+({src_host}[^\s]+)\s+\{\"Alert\":""",
  """"severity":\s*"({alert_severity}[^"]+)"""",
  """"subject":\s*"({alert_name}[^"]+)"""",
  """"type":\s*"({alert_type}[^"]+)"""",
  """"app":\s*"({alert_source}BOTsink):"""",
  """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
  """"src_category":\s*"({category}[^"]+)"""",
  """"body":\s*"({additional_info}[^"]+)""""
]
DupFields = ["alert_name->alert_subject"]
ParserVersion = "v1.0.0"


}
```