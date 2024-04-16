#### Parser Content
```Java
{
Name = "dropbox-d-json-app-file-success-tag"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ExtractionType = json
Conditions = [
"""".tag":"""
""""file_operations"}"""
""""event_category":"""
""""event_type":"""
]
Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.actor.user.display_name,exa_field_name=full_name"""
  """exa_json_path=$..email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.event_type.['.tag'],exa_field_name=operation"""
  """exa_json_path=$.event_type.description,exa_field_name=additional_info"""
  """exa_json_path=$..ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_regex=({app}Dropbox)"""
  """exa_json_path=$.assets..display_name,exa_field_name=object"""
  """exa_json_path=$.assets.contextual,exa_field_name=resource"""
]
ParserVersion = "v1.0.0"


}
```