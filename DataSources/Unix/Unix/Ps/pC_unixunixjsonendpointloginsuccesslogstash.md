#### Parser Content
```Java
{
Name = unix-unix-json-endpoint-login-success-logstash
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "epoch_sec"
  Conditions = ["""logstash-auditbeat""", """"process"""",  """"op":"login"""", """authentication""", """success"""]
  Fields = [
    """"end":({time}\d+)""",
    """"actor":\{.*?"secondary":"(|({user}[^"]+))""""
    """"actor":\{.*?"primary":"(|({account}[^"]+))""""
    """"user":\{.*?"uid":"({user_id}\d+)"""",
    """"user":\{.*?"gid":"({group_id}\d+)"""",
    """"pid":({process_id}\d+)""",
    """"ppid":({parent_process_id}\d+)""",
    """"process":\{.*?"name":"(|({process_name}[^"]+))"""",
    """"process":\{.*?"args":\[({arg}[^\[\]]+?)\]""",
    """"process":\{.*?"title":"({process_command_line}.*?)"(\}|,)"""
    """"host":\{.*?"name":"(|({host}[^"]+))"""",
    """"data":\{.*?"hostname":"(eth\d+\.)?(|({src_host}[^"]+))"""",
    """"result":"({result}[^"]+)"""",
    """"event":\{.*?"type":"(|({operation_type}[^"]+))"""",
    """"event":\{.*?"action":"(|({event_category}[^"]+))"""",
    """"event":\{.*?"category":"(|({event_subtype}[^"]+))"""",
    """"event":\{.*?"outcome":"(|({result}[^"]+))"""",
    """"source":\{"ip":"({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """"process":\{.*?"executable":"(|({service_name}[^"]+))"""",
    """"file":\{.*?"path":"(|({file_path}[^"]+))"""",
    """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
 ]
 DupFields = [ "host->dest_host" ]


}
```