#### Parser Content
```Java
{
Name = symantec-atp-json-alert-trigger-8003006
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  TimeFormat = "epoch"
  Conditions = [ """"event_id":8003006""", """"type_id":8003""", """"Symantec Endpoint Detection and Response"""", """collector_device_ip""" ]
  Fields = [
    """"(start_)?time":({time}\d{13})""",
    """collector_device_name":"({host}[^"]+)"""",
    """"path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))"""",
    """user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[^"]+))"""",
    """user_domain":"(NT AUTHORITY|({domain}[^"]+))"""",
    """"device_name":"({src_host}[^"]+)"""",
  """"device_os_name":"({os}[^",]+)"""",
    """"message":"({additional_info}[^"]+)"""",
    """device_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """src_port":({src_port}\d+)""",
    """dst_port":({dest_port}\d+)""",
    """dst_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """md5":"({hash_md5}[^"]+)"""",
    """event_id":({event_code}\d+)""",
    """size":({bytes}\d+)""",
    """cmd_line":"({process_command_line}[^\n]+?)\s*","""
  ]
  ParserVersion = "v1.0.0"


}
```