#### Parser Content
```Java
{
Name = "unix-unix-json-file-read-success-fileaccess"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""tags":["file_access""""
]
ParserVersion = "v1.0.0"

unix-activity-json.Fields}[
    """(I|i)nvalid user (({domain}[^\\:]+)\\+)?({user}[\w.'\-\\$]+)""",
    """from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"
},

{
Name = "unix-unixauditd-kv-group-member-remove-success-usermgmt"
Vendor = "Unix"
Product = "Unix Auditd"
TimeFormat = "epoch_sec"
Conditions = [
"""type=USER_MGMT"""
"""op=delete-user-from-group"""
"""res=success"""
]
Fields = [
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sacct="({account_name}[^"]+)""""
"""\sauid="?({account_id}\d+)"""
"""\sgrp="({group_name}[^"]+)""""
"""\suid=({user_id}\d+)"""
"""\sses=({session_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},

{
  Name = unix-auditbeat-json-process-create-success-processstarted
  Vendor = Unix
  Product = Auditbeat
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""auditbeat"""",""""action":"process_started"""",""""process":""",""""pid":"""]
  Fields = [
    """timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"hostname":"({host}[^"]+)""""
    """"action":"({event_name}[^"]+)"""",
    """"pid":({process_id}\d+)""",
    """"process".+?"executable":"({process_path}(({process_dir}[^"]*?)\/)?[^"\\\/]*?)"""",
    """"process":.+?"name":"({process_name}[^"]+)"""",
    """"ppid":({parent_process_id}\d+)""",
    """"message":"({additional_info}[^"]+)"""",
    """"args":\["({process_command_line}[^"]+)""""
    """"md5":"({hash_md5}[^"]+)"""",
    """user.+?group":.+?id":"({user_id}\d+)"""",
    """user.+?group":.+?name":"({user}[^"]+)""""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"
},

{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
""""end":({time}\d{10})"""
""""actor":\{.*?\"secondary\":\"(|({user}[^\"]+))\""""
""""actor":\{.*?\"primary\":\"(|({account}[^\"]+))\""""
""""user":\{.*?\"uid\":\"({user_id}\d+)\""""
""""user":\{.*?\"gid\":\"({group_id}\d+)\""""
""""pid":({process_id}\d+)"""
""""ppid":({parent_process_id}\d+)"""
""""process":\{.*?\"name\":\"(|({process_name}[^\"]+))\""""
""""process":\{.*?\"args\":\[({arg}[^\[\]]+?)\]"""
""""process":\{.*?\"title\":\"({process_command_line}.*?)\"(\}|,)"""
""""host":\{.*?\"name\":\"(|({dest_host}[^\"]+))\""""
""""data":\{.*?\"hostname\":\"(eth\d+\.)?(|({src_host}[^\"]+))\""""
""""result":\"({result}[^\"]+)\""""
""""event":\{.*?\"type\":\"(|({operation_type}[^\"]+))\""""
""""event":\{.*?\"action\":\"(|({event_category}[^\"]+))\""""
""""event":\{.*?\"category\":\"(|({event_subtype}[^\"]+))\""""
""""event":\{.*?\"result\":\"(|({result}[^\"]+))\""""
""""source":\{\"ip\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""process":\{.*?\"executable\":\"(|({service_name}[^\"]+))\""""
""""file":\{.*?\"path\":\"(|({file_path}[^\"]+))\""""
""""file":\{.*?\"owner\":\"(|({file_owner}[^\"]+))\""""
]
DupFields = [
"process_path->path"
"dest_host->host"
]
Name = "unix-unix-json-ssh-traffic-success-process"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""op":"PAM:authentication""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Unix
Product = Unix
TimeFormat = "epoch_sec"
Fields = [
  """"end":({time}\d{10})"""
  """"actor":\{.*?"secondary":"(|({user}[^"]+))""""
  """"actor":\{.*?"primary":"(|({account}[^"]+))""""
  """"user":\{.*?"uid":"({user_id}\d+)""""
  """"user":\{.*?"gid":"({group_id}\d+)""""
  """"pid":({process_id}\d+)"""
  """"ppid":({parent_process_id}\d+)"""
  """"process":\{.*?"name":"(|({process_name}[^"]+))""""
  """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
  """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
  """"host":\{.*?"name":"(|({host}[^"]+))""""
  """"data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
  """"result":"({result}[^"]+)""""
  """"event":\{.*?"type":"(|({operation_type}[^"]+))""""
  """"event":\{.*?"action":"(|({event_category}[^"]+))""""
  """"event":\{.*?"category":"(|({event_subtype}[^"]+))""""
  """"event":\{.*?"outcome":"(|({result}[^"]+))""""
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"process":\{.*?"executable":"(|({service_name}[^"]+))""""
  """"file":\{.*?"path":"(|({file_path}[^"]+))""""
  """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
  """({alert_name}susp_activity)"""
]
DupFields = [
  "alert_name->alert_type"
]
Name = unix-unix-json-alert-trigger-success-suspactivity
Conditions = [
  """logstash-auditbeat"""
  """"process""""
  """"tags":["susp_activity""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Unix
Product = Unix
TimeFormat = "epoch_sec"
Fields = [
  """"end":({time}\d{10})"""
  """"actor":\{.*?"secondary":"(|({user}[^"]+))""""
  """"actor":\{.*?"primary":"(|({account}[^"]+))""""
  """"user":\{.*?"uid":"({user_id}\d+)""""
  """"user":\{.*?"gid":"({group_id}\d+)""""
  """"pid":({process_id}\d+)"""
  """"ppid":({parent_process_id}\d+)"""
  """"process":\{.*?"name":"(|({process_name}[^"]+))""""
  """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
  """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
  """"host":\{.*?"name":"(|({host}[^"]+))""""
  """"data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
  """"result":"({result}[^"]+)""""
  """"event":\{.*?"type":"(|({operation_type}[^"]+))""""
  """"event":\{.*?"action":"(|({event_category}[^"]+))""""
  """"event":\{.*?"category":"(|({event_subtype}[^"]+))""""
  """"event":\{.*?"outcome":"(|({result}[^"]+))""""
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"process":\{.*?"executable":"(|({service_name}[^"]+))""""
  """"file":\{.*?"path":"(|({file_path}[^"]+))""""
  """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
  """({alert_name}unauthedfileaccess)"""
]
DupFields = [
  "alert_name->alert_type"
]
Name = unix-unix-json-alert-trigger-success-unauthedfileaccess
Conditions = [
  """logstash-auditbeat"""
  """"process""""
  """"tags":["unauthedfileaccess""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Unix
Product = Unix
TimeFormat = "epoch_sec"
Fields = [
  """"end":({time}\d{10})"""
  """"actor":\{.*?"secondary":"(|({user}[^"]+))""""
  """"actor":\{.*?"primary":"(|({account}[^"]+))""""
  """"user":\{.*?"uid":"({user_id}\d+)""""
  """"user":\{.*?"gid":"({group_id}\d+)""""
  """"pid":({process_id}\d+)"""
  """"ppid":({parent_process_id}\d+)"""
  """"process":\{.*?"name":"(|({process_name}[^"]+))""""
  """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
  """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
  """"host":\{.*?"name":"(|({host}[^"]+))""""
  """"data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
  """"result":"({result}[^"]+)""""
  """"event":\{.*?"type":"(|({operation_type}[^"]+))""""
  """"event":\{.*?"action":"(|({event_category}[^"]+))""""
  """"event":\{.*?"category":"(|({event_subtype}[^"]+))""""
  """"event":\{.*?"outcome":"(|({result}[^"]+))""""
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"process":\{.*?"executable":"(|({service_name}[^"]+))""""
  """"file":\{.*?"path":"(|({file_path}[^"]+))""""
  """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
  """({alert_name}recon)"""
]
DupFields = [
  "alert_name->alert_type"
]
Name = unix-unix-json-alert-trigger-success-recon
Conditions = [
  """logstash-auditbeat"""
  """"process""""
  """"tags":["recon""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Unix
Product = Unix
TimeFormat = "epoch_sec"
Fields = [
  """"end":({time}\d{10})"""
  """"actor":\{.*?"secondary":"(|({user}[^"]+))""""
  """"actor":\{.*?"primary":"(|({account}[^"]+))""""
  """"user":\{.*?"uid":"({user_id}\d+)""""
  """"user":\{.*?"gid":"({group_id}\d+)""""
  """"pid":({process_id}\d+)"""
  """"ppid":({parent_process_id}\d+)"""
  """"process":\{.*?"name":"(|({process_name}[^"]+))""""
  """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
  """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
  """"host":\{.*?"name":"(|({host}[^"]+))""""
  """"data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
  """"result":"({result}[^"]+)""""
  """"event":\{.*?"type":"(|({operation_type}[^"]+))""""
  """"event":\{.*?"action":"(|({event_category}[^"]+))""""
  """"event":\{.*?"category":"(|({event_subtype}[^"]+))""""
  """"event":\{.*?"outcome":"(|({result}[^"]+))""""
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"process":\{.*?"executable":"(|({service_name}[^"]+))""""
  """"file":\{.*?"path":"(|({file_path}[^"]+))""""
  """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
  """({alert_name}power_abuse)"""
]
DupFields = [
  "alert_name->alert_type"
]
Name = unix-unix-json-alert-trigger-success-powerabuse
Conditions = [
  """logstash-auditbeat"""
  """"process""""
  """"tags":["power_abuse""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
  """"end":({time}\d{10})"""
  """"actor":\{.*?"secondary":"(|({user}[^"]+))""""
  """"actor":\{.*?"primary":"(|({dest_user}[^"]+))""""
  """"user":\{.*?"uid":"({user_id}\d+)""""
  """"user":\{.*?"gid":"({group_id}\d+)""""
  """"pid":({process_id}\d+)"""
  """"ppid":({parent_process_id}\d+)"""
  """"process":\{.*?"name":"(|({process_name}[^"]+))""""
  """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
  """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
  """"host":\{.*?"name":"(|({host}[^"]+))""""
  """"data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
  """"result":"({result}[^"]+)""""
  """"event":\{.*?"type":"(|({operation_type}[^"]+))""""
  """"event":\{.*?"action":"(|({event_category}[^"]+))""""
  """"event":\{.*?"category":"(|({event_subtype}[^"]+))""""
  """"event":\{.*?"outcome":"(|({result}[^"]+))""""
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"process":\{.*?"executable":"(|({service_name}[^"]+))""""
  """"file":\{.*?"path":"(|({file_path}[^"]+))""""
  """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
]
DupFields = [
  "host->dest_host"
]
Name = unix-unix-json-user-switch-success-process
Conditions = [
  """logstash-auditbeat"""
  """"process""""
  """priv_esc"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
""""end":({time}\d{10})"""
""""actor":\{.*?"secondary":"(|({user}[^"]+))""""
""""actor":\{.*?"primary":"(|({account}[^"]+))""""
""""user":\{.*?"uid":"({user_id}\d+)""""
""""user":\{.*?"gid":"({group_id}\d+)""""
""""pid":({process_id}\d+)"""
""""ppid":({parent_process_id}\d+)"""
""""process":\{.*?"name":"(|({process_name}[^"]+))""""
""""process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
""""process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
""""host":\{.*?"name":"(|({host}[^"]+))""""
""""data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
""""result":"({result}[^"]+)""""
""""event":\{.*?"type":"(|({operation_type}[^"]+))""""
""""event":\{.*?"action":"(|({event_category}[^"]+))""""
""""event":\{.*?"category":"(|({event_subtype}[^"]+))""""
""""event":\{.*?"outcome":"(|({result}[^"]+))""""
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""process":\{.*?"executable":"(|({service_name}[^"]+))""""
""""file":\{.*?"path":"(|({file_path}[^"]+))""""
""""file":\{.*?"owner":"(|({file_owner}[^"]+))""""
]
DupFields = [
"process_path->path"
"host->dest_host"
]
Name = "unix-unix-json-file-read-success-fileaccess"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""tags":["file_access""""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
""""end":({time}\d{10})"""
""""actor":\{.*?"secondary":"(|({user}[^"]+))""""
""""actor":\{.*?"primary":"(|({account}[^"]+))""""
""""user":\{.*?"uid":"({user_id}\d+)""""
""""user":\{.*?"gid":"({group_id}\d+)""""
""""pid":({process_id}\d+)"""
""""ppid":({parent_process_id}\d+)"""
""""process":\{.*?"name":"(|({process_name}[^"]+))""""
""""process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
""""process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
""""host":\{.*?"name":"(|({host}[^"]+))""""
""""data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
""""result":"({result}[^"]+)""""
""""event":\{.*?"type":"(|({operation_type}[^"]+))""""
""""event":\{.*?"action":"(|({event_category}[^"]+))""""
""""event":\{.*?"category":"(|({event_subtype}[^"]+))""""
""""event":\{.*?"outcome":"(|({result}[^"]+))""""
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""process":\{.*?"executable":"(|({service_name}[^"]+))""""
""""file":\{.*?"path":"(|({file_path}[^"]+))""""
""""file":\{.*?"owner":"(|({file_owner}[^"]+))""""
]
DupFields = [
"process_dir->directory"
"process_path->path"
"host->dest_host"
]
Name = "unix-unix-json-file-permission-modify-success-permissionmodify"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""tags":["perm_mod""""
"""changed-file-permissions-of"""
]
ParserVersion = "v1.0.0"
}


{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
""""end":({time}\d{10})"""
""""actor":\{.*?"secondary":"(|({user}[^"]+))""""
""""actor":\{.*?"primary":"(|({account}[^"]+))""""
""""user":\{.*?"uid":"({user_id}\d+)""""
""""user":\{.*?"gid":"({group_id}\d+)""""
""""pid":({process_id}\d+)"""
""""ppid":({parent_process_id}\d+)"""
""""process":\{.*?"name":"(|({process_name}[^"]+))""""
""""process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
""""process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
""""host":\{.*?"name":"(|({host}[^"]+))""""
""""data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
""""result":"({result}[^"]+)""""
""""event":\{.*?"type":"(|({operation_type}[^"]+))""""
""""event":\{.*?"action":"(|({event_category}[^"]+))""""
""""event":\{.*?"category":"(|({event_subtype}[^"]+))""""
""""event":\{.*?"outcome":"(|({result}[^"]+))""""
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""process":\{.*?"executable":"(|({service_name}[^"]+))""""
""""file":\{.*?"path":"(|({file_path}[^"]+))""""
""""file":\{.*?"owner":"(|({file_owner}[^"]+))""""
]
DupFields = [
"process_path->path"
"host->dest_host"
]
Name = "unix-unix-json-file-success-logstashfile"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""tags":["file_"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
""""end":({time}\d{10})"""
""""actor":\{.*?"secondary":"(|({user}[^"]+))""""
""""actor":\{.*?"primary":"(|({account}[^"]+))""""
""""user":\{.*?"uid":"({user_id}\d+)""""
""""user":\{.*?"gid":"({group_id}\d+)""""
""""pid":({process_id}\d+)"""
""""ppid":({parent_process_id}\d+)"""
""""process":\{.*?"name":"(|({process_name}[^"]+))""""
""""process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
""""process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
""""host":\{.*?"name":"(|({host}[^"]+))""""
""""data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
""""result":"({result}[^"]+)""""
""""event":\{.*?"type":"(|({operation_type}[^"]+))""""
""""event":\{.*?"action":"(|({event_category}[^"]+))""""
""""event":\{.*?"category":"(|({event_subtype}[^"]+))""""
""""event":\{.*?"outcome":"(|({result}[^"]+))""""
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""process":\{.*?"executable":"(|({service_name}[^"]+))""""
""""file":\{.*?"path":"(|({src_file_path}[^"]+))""""
""""file":\{.*?"owner":"(|({file_owner}[^"]+))""""
]
DupFields = [
"process_path->path"
"host->dest_host"
]
Name = "unix-unix-json-file-success-logstashfile-1"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""tags":["perm_mod""""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Fields = [
""""end":({time}\d{10})"""
""""actor":\{.*?"secondary":"(|({user}[^"]+))""""
""""actor":\{.*?"primary":"(|({account}[^"]+))""""
""""user":\{.*?"uid":"({user_id}\d+)""""
""""user":\{.*?"gid":"({group_id}\d+)""""
""""pid":({process_id}\d+)"""
""""ppid":({parent_process_id}\d+)"""
""""process":\{.*?"name":"(|({process_name}[^"]+))""""
""""process":\{.*?"args":\[({arg}[^\[\]]+?)\]"""
""""process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
""""host":\{.*?"name":"(|({host}[^"]+))""""
""""data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))""""
""""result":"({result}[^"]+)""""
""""event":\{.*?"type":"(|({operation_type}[^"]+))""""
""""event":\{.*?"action":"(|({event_category}[^"]+))""""
""""event":\{.*?"category":"(|({event_subtype}[^"]+))""""
""""event":\{.*?"outcome":"(|({result}[^"]+))""""
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""process":\{.*?"executable":"(|({service_name}[^"]+))""""
""""file":\{.*?"path":"(|({file_path}[^"]+))""""
""""file":\{.*?"owner":"(|({file_owner}[^"]+))""""
]
DupFields = [
"process_path->path"
"host->dest_host"
]
Name = "unix-unix-json-file-success-logstashfile-2"
Conditions = [
"""logstash-auditbeat"""
""""process""""
""""opened-file""""
]
ParserVersion = "v1.0.0"
},

{
Name = "infoblox-bddi-str-dns-request-success-dnsquery"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
Conditions = [
""": query: """
"""named["""
]
Fields = [
  """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)""",
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
  """client\s*(::ffff:)?({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})#({src_port}\d+)(?:)""",
  """query:\s*({dns_query}\S+)\s"""
  """\sIN\s({dns_query_type}\w{1,5})\s""",
  """\s+IN\s.+?\s+({dns_query_flags}[^\d\w].*?)\s""",
  """response:\s*({dns_response_code}[^\s]+)\s""",
  """IN\s*.+?s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """ CNAME ({cname}[^;]+?)\.?;""",
]
ParserVersion = "v1.0.0"
},

{
  Name = unix-unix-json-process-create-auditd
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""type":"syscall"""", """auditd"""]
  Fields = [
    """"@timestamp":"({time}[^"]+)""",
    """"name_map":\{.*?"uid":"(|({user}[^"]+))"""",
    """"name_map":\{.*?"suid":"(|({account}[^"]+))"""",
    """"user":\{.*?"uid":"({user_id}\d+)"""",
    """"user":\{.*?"auid":"({account_id}\d+)"""",
    """"user":\{.*?"gid":"({group_id}\d+)"""",
    """"pid":"({process_id}\d+)""",
    """"ppid":"({parent_process_id}\d+)""",
    """"process":\{.*?"name":"(|({process_name}[^"]+))"""",
    """"process":\{.*?"exe":"(|({process_path}({process_dir}[^"]+\/).*?))"""",
    """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]""",
    """"host":\{.*?"name":"(|({host}[^"]+))"""",
    """"result":"({result}[^"]+)"""",
    """"event":\{.*?"type":"(|({operation_type}[^"]+))""""
 ]
 DupFields = ["host->dest_host"]
 ParserVersion = "v1.0.0"
},

{
Name = "unix-unix-kv-endpoint-authentication-success-dsepamauth"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""(dsepam:auth):"""
"""authentication success;"""
]
Fields = [
"""({time}\w+ \d+ \d\d:\d\d:\d\d)\s+({host}\S+)\s+\S+\s+\S+\(dsepam:auth\)"""
"""\suser=({user}.+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "ftp-f-str-file-delete-success-200"
Vendor = "FTP"
Product = "FTP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""]dele """
""" - 200 - - - """
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) """
"""({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]"""
"""({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]"""
"""(-|(({domain}\S+)[\/\\])?({user}\S+))\s+\[\d+\]"""
"""\]dele\s+(-|({file_name}\S+))\s"""
"""\]dele\s+(-|({file_path}({file_dir}\/(\S+\/)?)({file_name}\S+)))\s"""
"""\]dele\s+\/\S+\.({file_ext}[^\/\.\s]+)\s"""
"""\]dele\s+(\S+\s+){2}({result}\d+)"""
]
DupFields = [
"host->dest_host"
"file_ext->host_file_ext"
]
ParserVersion = "v1.0.0"
},

{
  Name = delinea-centrifyis-kv-process-create-success-unixname
  Vendor = Delinea
  Product = Centrify Infrastructure Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ MachineName: """", """ UnixName: """", """Command:""" ]
  Fields = [
    """Time:\s*"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """MachineName:\s*"+({host}[\w\-.]+)""",
    """Command:\s*"+({process_command_line}[^"]+)""",
    """Command:\s*"+({process_path}({process_dir}[^\s"]*?)[\\\/]*({process_name}[^\\\/\s"]+))""",
    """UserName:\s*"+({user}[^"]+)""",
    """UnixName:\s*"+({account}[^"]+)""",
    """ClientName:\s*"+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^"]+))""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"
},

${UnixParsersTemplates.cef-unix-template-1}{
  Name = unix-unixauditd-cef-process-create-success-execve
  Conditions = [ """CEF""", """Unix|auditd""", """EXECVE""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\""",
    """Arguments:\s*({process_command_line}.*?)\s*cs1Label="""
  ]
  ParserVersion = "v1.0.0"
},

${UnixParsersTemplates.cef-unix-template-1}{
  Name = unix-unixauditd-cef-process-create-success-syscall
  Conditions = [ """CEF""", """Unix|auditd""", """SYSCALL""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """CEF:([^\|]*\|){5}({event_name}[^\\\|]+)\|({result}[^\|]+)"""
  ]
  ParserVersion = "v1.0.0"
},

${UnixParsersTemplates.cef-unix-template-1}{
  Name = unix-unixauditd-cef-process-create-success-usercmd
  Conditions = [ """CEF""", """Unix|auditd""", """USER_CMD""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """cmd\\=({command}[^\s]+)""",
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\"""
  ]
  ParserVersion = "v1.0.0"
},
{
  Name = unix-ad-cef-endpoint-login-success-userauth
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Unix|auditd|""", """|USER_AUTH\|success|""", """sshd"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\soutcome=({result}.+?)\s+\w+=""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\saddr\\=(?:\?|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\shostname\\=(?:\?|(src_host)\S+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sshost=({src_host}\S+)""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sact=({auth}\S.+?)\s+\w+=""",
    """\sdproc=({auth_process}\S.+?)\s+\w+=""",
    """({event_code}ssh)""",
  ]
  DupFields = [ "host->dest_host" 
}
```