#### Parser Content
```Java
{
Name = "symantec-atp-json-file-write-success-8003-1"
Conditions = [
""""event_id":8003004"""
""""type_id":8003"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"

symantec-usb-activity.Fields}[
     """device":"({device_id}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"
}

{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
]
Name = "symantec-atp-json-file-delete-success-8003"
Conditions = [
""""event_id":8003002"""
""""type_id":8003"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
"""({file_type}directory)"""
]
Name = "symantec-atp-json-file-delete-success-8004"
Conditions = [
""""event_id":8004002"""
""""type_id":8004"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
]
Name = "symantec-atp-json-file-write-success-8003"
Conditions = [
""""event_id":8003001"""
""""type_id":8003"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
]
Name = "symantec-atp-json-file-write-success-8003-1"
Conditions = [
""""event_id":8003004"""
""""type_id":8003"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
]
Name = "symantec-atp-json-file-write-success-8003-2"
Conditions = [
""""event_id":8003005"""
""""type_id":8003"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
"""({file_type}directory)"""
]
Name = "symantec-atp-json-file-write-success-8003-3"
Conditions = [
""""event_id":8004001"""
""""type_id":8004"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Symantec"
Product = "Symantec Advanced Threat Protection"
TimeFormat = "epoch"
Fields = [
""""(start_)?time":({time}\d{13})"""
"""collector_device_name":"({host}[^"]+)""""
""""path":"({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))?))""""
"""user_name":"((?i)(LOCAL SERVICE|SYSTEM|NETWORK SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""user_domain":"(NT AUTHORITY|({domain}[^"]+))""""
""""device_name":"({src_host}[^"]+)""""
""""message":"({additional_info}[^"]+)""""
"""device_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port":({src_port}\d+)"""
"""dst_port":({dest_port}\d+)"""
"""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""md5":"({hash_md5}[^"]+)""""
"""event_id":({event_code}\d+)"""
"""size":({bytes}\d+)"""
"""cmd_line":"({process_command_line}[^\n]+?)\s*","""
"""({file_type}directory)"""
]
Name = "symantec-atp-json-file-write-success-8003-4"
Conditions = [
""""event_id":8004004"""
""""type_id":8004"""
""""Symantec Endpoint Detection and Response""""
"""collector_device_ip"""
]
ParserVersion = "v1.0.0"
},

{
  Name = symantec-wss-sk4-http-session-observed
  Vendor = Symantec
  Product = Symantec Web Security Service
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd, HH:mm:ss"
  Conditions = [ """destinationServiceName =Symantec WSS""", """, OBSERVED,"""]
  Fields = [
    """cs6=\[[^,]+,\s({time}\d\d\d\d-\d\d-\d\d,\s\d\d:\d\d:\d\d)""",
    """cs6=\[([^,]+,){3}\s({host}[^,]+)""",
    """\sdproc=(|({process_name}[^=]+?))\s+\w+=""",
    """,\s(Unauthenticated User|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(,\s[^,]+){2},\sOBSERVED""",
    """,\s({action}OBSERVED),""".
    """,\sOBSERVED,\s(-|({category}[^,]+))""",
    """,\sOBSERVED(,\s([^,]+)),\s(-|({referrer}[^\s,]+))""",
    """,\sOBSERVED(,\s([^,]+)){2},\s(-|({result_code}\d{1,3}))""",
    """,\sOBSERVED(,\s([^,]+)){3},\s(-|unknown|({proxy_action}[^,]+))""",
    """,\sOBSERVED(,\s([^,]+)){4},\s(-|unknown|({method}[^,]+))""",
    """,\sOBSERVED(,\s([^,]+)){5},\s(-|({mime}[^,]+))""",
    """,\sOBSERVED(,\s([^,]+)){6},\s(-|({protocol}[^,]+))""",
    """,\sOBSERVED(,\s([^,]+)){7},\s(-|({url}[^\s,]+))""",
    """,\sOBSERVED(,\s([^,]+)){8},\s(-|({dest_port}\d{1,5}))""",
    """,\sOBSERVED(,\s([^,]+)){9},\s(-|({uri_path}\/[^\s,]*))""",
    """,\sOBSERVED(,\s([^,]+)){10},\s(-|({uri_query}\?[^\s,]*))""",
    """,\sOBSERVED(,\s([^,]+)){12},\s(-|({user_agent}[^,]+))""",
    """,\sOBSERVED(,\s([^,]+)){13},\s(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),""",
    """,\sOBSERVED(,\s([^,]+)){25,26},\s(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),"""
    """OBSERVED(,\s+[^,]+){25},\s+(-,\s)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(,\s+[^,]+){28},\s+(-|({src_host}[\w.-]+))"""
    """(OBSERVED|PROXIED|DENIED)(,\s+[^,]+){65},\s+(-,\s)?(?:-|({transaction_id}[^,"\]]+))"""
    """,\s*(-|({additional_info}[^,]+)),?\s*(OBSERVED|PROXIED|DENIED)"""
  ]
  DupFields = ["result_code->http_response_code"
}
```