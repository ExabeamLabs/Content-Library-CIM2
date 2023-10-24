#### Parser Content
```Java
{
Name = code42-incydr-json-file-succes-file
  Vendor = Code42
  Product = Code42 Incydr
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions= [ """"action":""", """"file":{""", """Code42""",""""source":{""",""""destination":{""" ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"action":"({event_name}[^"]+)"""",
    """"user":\s*\{"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"file":\s*\{"name":"({file_name}[^"]+?(\.({file_ext}[^"\.]+))?)"""",
    """"file"[^\}]+?"directory":"({file_dir}[^"]+)"""",
    """"file":\s*\{.+?"originalDirectory":"({src_file_dir}[^"]+)""""
    """"file"[^\}]+?"category":"({file_type}[^"]+)"""",
    """"file":\s*\{.+?"originalName":"({src_file_name}[^"\.]+(\.({src_file_ext}[^"]+))?)"""",
    """"file"[^\}]+?"sizeInBytes":(({bytes}\d+))""",
    """"source":[^\}]+?"name":\s*"({src_host}[\w\-.]+)"""",
    """"source":\{.+?"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"domain":"({domain}[^"]+)"""",
    """"busType":"({device_type}[^"]+)"""",
    """"mediaName":"({device_name}[^"]+)"""",
    """"serialNumber":"({removable_media_serial_number}[^"]+)"""",
    """"changeType":"(NONE|({operation}[^"]+))"""",
    """"hash":\s*[^\}]+?"md5":"({hash_md5}[^"]+)"""",
    """"hash":\s*[^\}]+?"sha256":"({hash_sha256}[^"]+)"""",
    """"repositoryUri":"([^:]+:)?({repository_name}[^"]+)"""",
    """"printerName":"({printer_name}[^"]+)""""
    """"printJobName":"({object}[^"]+)""""
    """"severity":"({alert_severity}[^"]+)"""",
    """"operatingSystem":"({os}[^"]+)""",
    """"file"[^\}]+?"category":"({file_category}[^"]+)"""",
    """"file"[^\}]+?"mimeTypeByBytes":"({mime}[^"]+)"""",
    """"file"[^\}]+?"owner":"([^\\]+\\+)?({file_owner}[^"]+)""""
    """"file".+?"url":"({file_url}[^"]+)"""",
    """"process"[^\}]+?"executable":"({process_path}[^"]+)"""",
    """"destination"[^\}]+"user":\s*\{"email":\[\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"destination"[^\}]+"category":"({dest_group}[^"]+)"""",
  ]


}
```