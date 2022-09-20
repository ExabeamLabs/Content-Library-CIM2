#### Parser Content
```Java
{
Name = symantec-edr-json-process-create-success-8001001
  Vendor = Symantec
  Product = Symantec EDR
  TimeFormat = "epoch"
  Conditions = [ """"event_id":8001001""", """"type_id":8001""", """"Symantec Endpoint Detection and Response"""", """collector_device_ip""" ]
  Fields = [
    """"(start_)?time":({time}\d+)""",
    """collector_device_name":"({host}[^"]+)"""",
    """"path":"({process_path}({process_dir}(?:[^";]+)?[\\\/;])?({process_name}[^\\\/";]+?))"""",
    """user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[^"]+))"""",
    """user_domain":"(NT AUTHORITY|({domain}[^"]+))"""",
    """"device_name":"({src_host}[^"]+)"""",
    """"message":"({additional_info}[^"]+)"""",
    """device_ip":"({src_ip}[a-fA-F\d:.]+)"""",
    """src_ip":"({src_ip}[a-fA-F\d:.]+)""""
    """src_port":({src_port}\d+)""",
    """dst_port":({dest_port}\d+)""",
    """dst_ip":"({dest_ip}[a-fA-F\d:.]+)"""",
    """md5":"({hash_md5}[^"]+)"""",
    """event_id":({event_code}\d+)""",
    """size":({bytes}\d+)""",
    """cmd_line":"({process_command_line}[^\n]+?)\s*","""
  ]
  ParserVersion = "v1.0.0"


}
```