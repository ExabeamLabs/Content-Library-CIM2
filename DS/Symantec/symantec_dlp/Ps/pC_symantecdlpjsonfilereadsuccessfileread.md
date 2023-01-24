#### Parser Content
```Java
{
Name = symantec-dlp-json-file-read-success-fileread
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """type":"""", ""","device":"""", """"action":"File Read"""" ]
  Fields = [
    """device":"({device_id}[^"]+)""",
	"""\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s""",
    """"@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
    """"hostname":"({dest_host}[\w\-.]+)""",
    """"action":"({operation}[^"]+)""",
    """"user":\{"name":"(system|({user}[^"\s]+))"""",
    """"ip":"(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"executable":"({process_path}({process_dir}(?:[^,"]+)?[\\\/])?({process_name}[^\\\/,"]+?))"""",
    """"path":"(|({file_path}({file_dir}[^"]*?[\\\/]*)(|({file_name}[^\\\/"]*?(\.({file_ext}[^\\\/\.\s"]*))?))))\s*"""",
    """"size":({bytes}\d+)""",
    """({device_type}(CD-DVD|USB))""",
  ]
  ParserVersion = "v1.0.0"


}
```