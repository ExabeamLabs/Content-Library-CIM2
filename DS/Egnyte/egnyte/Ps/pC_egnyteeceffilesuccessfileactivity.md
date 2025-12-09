#### Parser Content
```Java
{
Name = "egnyte-e-cef-file-success-fileactivity"
Vendor = "Egnyte"
Product = "Egnyte"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"file/folder":""""
  """"target_path":""""
  """"transaction":""""
]
Fields = [
  """"username":"({full_name}[^"\(\)]+?)\s*\(\s*({email_address}[^@"\)]+@[^\\)"\.]+\.[^"\)]+?)\s*\)"""
  """"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*""""
  """"transaction":"({operation}[^"]+)"""
  """"target_path":"(N/A|({object}[^"]+))"""
  """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  """"access":"({service_name}[^"]+)"""
  """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({app}Egnyte)"""
]
ParserVersion = "v1.0.0"


}
```