#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-phonecreate
Vendor = Cisco
Product = "Cisco Identity and Access Management"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSSZ", "epoch_sec"]
Conditions = [
  """"action":"""
  """"object":"""
  """"username":"""
  """"description":"""
]
Fields = [
   """exa_json_path=$.timestamp,exa_regex=({time}\d{10})""",
  """exa_json_path=$.action,exa_field_name=operation""",
  """exa_json_path=$.object,exa_field_name=object""",
  """exa_json_path=$.description,exa_field_name=additional_info""",
  """exa_regex="username":"(({full_name}({first_name}[^\s":]+)\s({last_name}[^":]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
  """exa_regex="email\\"+:\s*\\"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\"+""",
  """exa_json_path=$.description,exa_regex="ip_address\\"+:\s*\\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\"+"""
]
ParserVersion = "v1.0.0"


}
```