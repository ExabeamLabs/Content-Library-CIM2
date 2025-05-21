#### Parser Content
```Java
{
Name = unix-auditbeat-json-group-create-success-addshadowgroup
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Auditbeat
  TimeFormat = "epoch_sec"
  Conditions = ["""logstash-auditbeat""", """"process"""",  """"op":"add-shadow-group""""]
  Fields = [
    """"end":({time}\d{10})""",
    """"actor":\{.*?"secondary":"(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
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
    """"source":\{"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"process":\{.*?"executable":"(|({service_name}[^"]+))"""",
    """"file":\{.*?"path":"(|({file_path}[^"]+))"""",
    """"file":\{.*?"owner":"(|({file_owner}[^"]+))""""
 ]
 DupFields = [ "host->dest_host" ]


}
```