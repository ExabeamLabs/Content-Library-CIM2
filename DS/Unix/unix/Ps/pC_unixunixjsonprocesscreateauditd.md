#### Parser Content
```Java
{
Name = unix-unix-json-process-create-auditd
  Vendor = Unix
  Product = Unix
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","epoch"]
  Conditions = [""""type":"syscall"""", """auditd"""]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.user.name_map.uid,exa_field_name=user""",
    """exa_json_path=$.user.name_map.suid,exa_field_name=account""",
    """exa_json_path=$.user.uid,exa_field_name=user_id""",
    """exa_json_path=$.user.auid,exa_field_name=account_id""",
    """exa_json_path=$.user.gid,exa_field_name=group_id""",
    """exa_json_path=$.process.pid,exa_field_name=process_id""",
    """exa_json_path=$.process.ppid,exa_field_name=parent_process_id""",
    """exa_json_path=$.process.name,exa_field_name=process_name""",
    """exa_json_path=$.process,exa_regex=\{.*?"exe":"(|({process_path}({process_dir}[^"]+\/).*?))"""",
    """exa_json_path=$.process.args,exa_field_name=arg""",
    """exa_json_path=$.host.name,exa_field_name=host""",
    """exa_json_path=$.auditd.result,exa_field_name=result""",
    """exa_json_path=$.event.type,exa_field_name=operation_type""",
    """"@timestamp":"({time}[^"]+)""",
    """"timestamp":"({time}[^"]+)""",
    """"name_map":\{.*?"uid":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
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
    """\{"audit":\s*\{.+?"pid":"({process_id}[^"]+)"""
    """\{"audit":\s*\{.+?"gid":"({group_id}[^"]+)"""
    """\{"audit":\s*\{.+?"ppid":"({parent_process_id}[^"]+)"""
    """\{"audit":\s*\{.+?"uid":"({user_id}[^"]+)"""
    """\{"audit":\s*\{.+?"command":"({process_command_line}[^"]+)"""
    """"success":"({result}[^"]+)"""
    """\{"audit":.+?"exe":"(|({process_path}({process_dir}[^"]+\/).*?))""""
 ]
 DupFields = ["host->dest_host"]
 ParserVersion = "v1.0.0"


}
```