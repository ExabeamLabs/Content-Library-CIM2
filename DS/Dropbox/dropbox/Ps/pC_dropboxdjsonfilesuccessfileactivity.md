#### Parser Content
```Java
{
Name = "dropbox-d-json-file-success-fileactivity"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"event_category": "files""""
  """"info_dict":"""
  """"event_type_description":"""
]
Fields = [
  """"name":\s*"(?:N\/A|({full_name}[^"@,]+))""""
  """"name":\s*"(?:N\/A|(({domain}[^"@\\\s]+)\\+)?({user}[^"@\\\s]+))""""
  """"email":\s*"(?:N\/A|({email_address}[^@"\s]+@[^@"\s]+))""""
  """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\d:+-]+)""""
  """"event_type":\s*"({event_subtype}[^"]+)""""
  """"event_type_description":\s*"({access}[^"]+)""""
  """"is_dir":\s*false,.*?({file_type}file)"""
  """"is_dir":\s*true,.*?({file_type}folder)"""
  """"({file_type}folder)_name":"""
  """"event_type_description":\s*"[^"]*?({file_type}link)""""
  """"ip_address":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"path":\s*"({file_path}({file_dir}[^"]+?\/?)?({file_name}[^"/]+?({file_ext}\.[^"\\\/\s\d\.]+)?))""""
  """"folder_name":\s*"({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)""""
  """"orig_folder_name":\s*"({src_file_name}[^"]+)""""
  """"doc_title":\s*"({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)""""
  """"doc_title":\s*"({object}[^"]+)""""
  """"file_name":\s*"({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```