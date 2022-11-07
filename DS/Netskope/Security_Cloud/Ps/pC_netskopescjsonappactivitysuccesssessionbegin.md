#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-success-sessionbegin
  Vendor = Netskope
  Product = Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [  """"session_begin"""",""""activity"""",""""object_id"""" ]
  Fields = [
    """"dstip": "({host}[^"]+)"""",
    """"timestamp": ({time}\d+)""",
    """"user": "({account}[^"]+)"""",
    """"app": "({app}[^"]+)"""",
    """"dstip": "({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"srcip": "({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"activity": "({operation}[^"]+)"""",
    """"from_user": "(?![^\s]+@[^\s]+)({user}[^"\s]+)"""",
    """"from_user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""",
    """"object": ["\\:, ]+({file_name}.+?)["\\:, ]+, """",
    """"object_type": "({file_type}[^"]+)"""",
    """"url": "({additional_info}[^"]+)""""
    """"browser": "(unknown|({user_agent}[^"]+))"""",
  ]
   DupFields=["file_name->object_value",
     "additional_info->file_dir",
     "operation->access"]
     ParserVersion = "v1.0.0"


}
```