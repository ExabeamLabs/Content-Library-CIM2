#### Parser Content
```Java
{
Name = symantec-atp-json-process-create-success-8001001
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  TimeFormat = "epoch"
  Conditions = [ """"event_id":8001001""", """"type_id":8001""", """"Symantec Endpoint Detection and Response"""", """collector_device_ip""" ]
  Fields = [
    """"(start_)?time":({time}\d{13})""",
    """collector_device_name":"({host}[^"]+)"""",
    """"path":"({process_path}({process_dir}(?:[^";]+)?[\\\/;])?({process_name}[^\\\/";]+?))"""",
    """user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-]{1,40}\$?))"""",
    """user_domain":"(NT AUTHORITY|({domain}[^"]+))"""",
    """"device_name":"({src_host}[^"]+)"""",
    """"message":"({additional_info}[^"]+)"""",
    """device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """src_port":({src_port}\d+)""",
    """dst_port":({dest_port}\d+)""",
    """dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """md5":"({hash_md5}[^"]+)"""",
    """event_id":({event_code}\d+)""",
    """size":({bytes}\d+)""",
    """cmd_line":"({process_command_line}[^\n]+?)\s*","""
  ]
  ParserVersion = "v1.0.0"


}
```