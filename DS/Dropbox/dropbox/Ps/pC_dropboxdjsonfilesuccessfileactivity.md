#### Parser Content
```Java
{
Name = "dropbox-d-json-file-success-fileactivity"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ExtractionType = json
Conditions = [
  """"event_category": "files""""
  """"info_dict":"""
  """"event_type_description":"""
]
Fields = [
  """exa_json_path=$.name,exa_field_name=full_name"""
  """exa_json_path=$.name,exa_regex=^(?:N\/A|(({domain}[^"@\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))$"""
  """exa_json_path=$..email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.time,exa_field_name=time"""
  """exa_json_path=$.event_type,exa_field_name=event_subtype"""
  """exa_json_path=$.event_type_description,exa_field_name=access"""
  """exa_json_path=$.is_dir,exa_field_name=file_type"""
  """exa_json_path=$.is_dir,exa_field_name=file_type"""
  """exa_json_path=$._name,exa_field_name=file_type"""
  """exa_json_path=$.event_category,exa_field_name=file_type"""
  """exa_json_path=$.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_regex="path":\s*"({file_path}({file_dir}[^"]+?\/?)?({file_name}[^"/]+?(\.({file_ext}[^"\\\/\s\d\.]+))?))""""
  """exa_json_path=$.folder_name,exa_regex=({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)"""
  """exa_json_path=$.orig_folder_name,exa_regex=({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)"""
  """exa_json_path=$.doc_title,exa_regex=({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)"""
  """exa_json_path=$.doc_title,exa_field_name=object"""
  """exa_json_path=$.file_name,exa_regex=({src_file_name}[^"]+?({src_file_ext}\.[^"\\\/\s\d\.]+)?)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```