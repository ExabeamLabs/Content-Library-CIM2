#### Parser Content
```Java
{
Name = unix-auditbeat-json-file-create-success-file
  Vendor = Unix
  Product = Auditbeat
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""auditbeat"""",""""action":""",""""category":["file"""]
  Fields = [
    """timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"host":.+?"name":"({host}[\w\-.]+?)(@[^"]*)?"""",
    """"hostname":"({dest_host}[\w\-.]+?)(@[^"]*)?"""",
    """"owner":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"path":"({file_path}({file_dir}[^\"]*?[\\\/]+)?\s*({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """"size":({bytes}\d+)""",
    """"action":\["({access}({action}[^"]+))"""",
    """"sha1":"({hash_sha1}[^"]+)""""
  ]


}
```