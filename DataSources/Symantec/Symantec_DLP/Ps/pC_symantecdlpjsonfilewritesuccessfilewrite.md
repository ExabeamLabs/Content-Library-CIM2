#### Parser Content
```Java
{
Name = symantec-dlp-json-file-write-success-filewrite
  Conditions = [ """type":"""", ""","device":"""", """"action":"File Write"""" ]
  Fields = ${SymantecParsersTemplates.symantec-usb-activity.Fields}[
     """device":"({device_id}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"

symantec-usb-activity = {
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s""",
      """"@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
      """"hostname":"({src_host}[\w\-.]+)""",
      """"action":"({operation}[^"]+)""",
      """"user":\{"name":"(system|({user}[^"\s]+))"""",
      """"ip":"(0.0.0.0|({dest_ip}[A-Fa-f:\d.]+))""",
      """"executable":"({process_path}({process_dir}(?:[^,"]+)?[\\\/])?({process_name}[^\\\/,"]+?))"""",
      """"path":"(|({src_file_path}({file_dir}[^"]*?[\\\/]*)(|({src_file_name}[^\\\/"]*?(\.({src_file_ext}[^\\\/\.\s"]*))?))))\s*"""",
      """"size":({bytes}\d+)""",
      """({device_type}(CD-DVD|USB))""",
    
}
```