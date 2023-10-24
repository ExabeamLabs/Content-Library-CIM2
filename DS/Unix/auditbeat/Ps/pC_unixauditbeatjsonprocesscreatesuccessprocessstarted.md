#### Parser Content
```Java
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
    """user.+?group":.+?name":"({user}[\w\.\-]{1,40}\$?)""""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```