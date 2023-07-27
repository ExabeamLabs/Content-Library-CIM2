#### Parser Content
```Java
{
Name = unix-auditbeat-json-process-create-fail-processerror
  Vendor = Unix
  Product = Auditbeat
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""auditbeat"""",""""action":"process_error"""",""""category":["process""",""""pid":"""]
  Fields = [
    """timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"host":.+?name":"({host}[^"]+)"""",
    """"action":"({event_name}[^"]+)"""",
    """"pid":({process_id}\d+)""",
    """"process".+?"executable":"({process_path}(({process_dir}[^"]*?)\/)?[^"\\\/]*?)"""",
    """"process":.+?"name":"({process_name}[^"]+)"""",
    """"ppid":({parent_process_id}\d+)""",
    """"message":"({failure_reason}[^"]+)"""",
    """user.+?group":.+?id":"({user_id}\d+)"""",
    """user.+?group":.+?name":"({user}[\w\.\-]{1,40}\$?)""""
  ]
  DupFields = ["host->dest_host"]


}
```