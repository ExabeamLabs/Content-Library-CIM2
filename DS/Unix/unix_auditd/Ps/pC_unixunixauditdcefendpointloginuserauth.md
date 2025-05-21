#### Parser Content
```Java
{
Name = "unix-unixauditd-cef-endpoint-login-userauth"
Conditions = [
"""CEF"""
"""Unix|auditd"""
"""USER_AUTH"""
]
ParserVersion = "v1.0.0"

unix-activity-json.Fields}[
    """exa_json_path=$.jsonPayload.message,exa_regex=(I|i)nvalid user (({domain}[^\\:]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.jsonPayload.message,exa_regex=from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.jsonPayload.message,exa_regex=\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
    """"hostname":"({host}[\w\-.]+?)(@[^"]*)?""""
    """"action":"({event_name}[^"]+)"""",
    """"pid":({process_id}\d+)""",
    """"process".+?"executable":"({process_path}(({process_dir}[^"]*?)\/)?[^"\\\/]*?)"""",
    """"process":.+?"name":"({process_name}[^"]+)"""",
    """"ppid":({parent_process_id}\d+)""",
    """"message":"({additional_info}[^"]+)"""",
    """"args":\["({process_command_line}[^"]+)""""
    """"md5":"({hash_md5}[^"]+)"""",
    """user.+?group":.+?id":"({user_id}\d+)"""",
    """user.+?group":.+?name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"
},

{
Vendor = Unix
Product = Unix
TimeFormat = "epoch_sec"
Fields = [
  """"end":({time}\d{10})"""
  """"actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
  """"actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
  """"actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
  """"actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
  """"actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
  """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
""""actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
""""actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
""""actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
""""actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
""""actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
""""source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
Vendor = "Unix"
Product = "Unix"
TimeFormat = [ "dd-MMM-yyyy HH:mm:ss.SSS", "MMM dd HH:mm:ss" ]
Conditions = [
""": query: """
"""named"""
]
Fields = [
  """\d\d:\d\d:\d\d(\.\d+Z?)? (::ffff:)?({host}[\w\.-]+)""",
  """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)""",
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
  """\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))#({src_port}\d+)(?:)""",
  """query:\s*({dns_query}\S+)\s"""
  """\sIN\s({dns_query_type}\w{1,5})\s""",
  """\s+IN\s.+?\s+({dns_query_flags}[^\d\w].*?)\s""",
  """response:\s*({dns_response_code}[^\s]+)\s""",
  """\sIN\s+.+?\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(;|$|"|\.|\))""",
  """ CNAME ({additional_info}[^;]+?)\.?;""",
  ]
ParserVersion = "v1.0.0"
},

{
Name = "unix-unix-kv-endpoint-authentication-success-dsepamauth"
Vendor = "Unix"
Product = "Unix"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
Conditions = [
"""(dsepam:auth):"""
"""authentication success;"""
]
Fields = [
"""({time}\w+ \d+ \d\d:\d\d:\d\d)\s+({host}\S+)\s+\S+\s+\S+\(dsepam:auth\)"""
"""\suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
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
"""(-|(({domain}\S+)[\/\\])?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\[\d+\]"""
"""\]dele\s+(-|({file_name}\S+))\s"""
"""\]dele\s+(-|({file_path}({file_dir}\/(\S+\/)?)({file_name}\S+)))\s"""
"""\]dele\s+\/\S+\.({file_ext}[^\/\.\s]+)\s"""
"""\]dele\s+(\S+\s+){2}({result}\d+)"""
]
DupFields = [
"host->dest_host"
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
    """\saddr\\=(?:\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\shostname\\=(?:\?|(src_host)\S+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sshost=({src_host}\S+)""",
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """\sact=({auth}\S.+?)\s+\w+=""",
    """\sdproc=({auth_process}\S.+?)\s+\w+=""",
    """({event_code}ssh)""",
  ]
  DupFields = [ "host->dest_host" 
}
```