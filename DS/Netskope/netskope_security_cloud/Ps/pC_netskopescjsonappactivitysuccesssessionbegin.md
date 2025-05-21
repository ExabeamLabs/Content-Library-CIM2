#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-success-sessionbegin
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [  """"session_begin"""",""""activity"""",""""object_id"""" ]
  Fields = [
    """"dstip": "({host}[^"]+)"""",
    """"timestamp": ({time}\d{10})""",
    """"user": "({account}[^"]+)"""",
    """"app": "({app}[^"]+)"""",
    """"dstip": "({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"srcip": "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"activity": "({operation}[^"]+)"""",
    """"from_user": "(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"from_user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""",
    """"object": ["\\:, ]+({file_name}.+?)["\\:, ]+, """",
    """"object_type": "({file_type}[^"]+)"""",
    """"url": "({additional_info}[^"]+)""""
    """"browser": "(unknown|({user_agent}[^"]+))"""",
  ]
   DupFields=[
     "file_name->object_value",
     "additional_info->file_dir",
     "operation->access"
   ]
   ParserVersion = "v1.0.0"


}
```