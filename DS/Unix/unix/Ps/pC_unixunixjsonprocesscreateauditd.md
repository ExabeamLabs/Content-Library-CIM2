#### Parser Content
```Java
{
Name = unix-unix-json-process-create-auditd
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""type":"syscall"""", """auditd"""]
  Fields = [
    """"@timestamp":"({time}[^"]+)""",
    """"name_map":\{.*?"uid":"(|({user}[\w\.\-]{1,40}\$?))"""",
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


}
```