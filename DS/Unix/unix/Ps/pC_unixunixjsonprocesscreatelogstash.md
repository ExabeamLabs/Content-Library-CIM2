#### Parser Content
```Java
{
Name = unix-unix-json-process-create-logstash
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""logstash-auditbeat""", """"process""""]
  Fields = [
    """"@timestamp":"({time}[^"]+)""",
    """"name_map":\{.*?"uid":"(|({user}[^"]+))"""",
    """"actor":\{[^\}]+?"secondary":"(|({user}[^"]+))""""
    """"actor":\{[^\}]+?"primary":"(|({account}[^"]+))""""
    """"name_map":\{.*?"suid":"(|({account}[^"]+))"""",
    """"user":\{.*?"uid":"({user_id}\d+)"""",
    """"user":\{.*?"auid":"({account_id}\d+)"""",
    """"user":\{.*?"gid":"({group_id}\d+)"""",
    """"pid":"({process_id}\d+)""",
    """"ppid":"({parent_process_id}\d+)""",
    """"process":\{.*?"name":"(|({process_name}[^"]+))"""",
    """"process":\{.*?"exe":"(|({process_path}({process_dir}[^"]+\/).*?))"""",
    """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]""",
    """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
    """"host":\{.*?"name":"(|({host}[^"]+))"""",
    """"result":"({result}[^"]+)"""",
    """"event":\{.*?"type":"(|({operation_type}[^"]+))"""",
    """"event":\{.*?"action":"(|({event_category}[^"]+))"""",
    """"event":\{.*?"category":"(|({event_subtype}[^"]+))"""",
    """"event":\{.*?"outcome":"(|({result}[^"]+))"""",
    """"hostname":"({src_host}[^"]+)"""",
 ]
 DupFields = [ "host->dest_host" ]
 ParserVersion = "v1.0.0"


}
```