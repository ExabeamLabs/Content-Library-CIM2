#### Parser Content
```Java
{
Name = "dropbox-d-json-app-activity-success-sharing-2"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ExtractionType = json
Conditions = [
  """"event_category": "sharing""""
  """"info_dict":"""
  """"event_type": "paper_doc_team_mention""""
]
Fields = [
  """exa_json_path=$.name,exa_field_name=full_name"""
  """exa_json_path=$.name,exa_regex=^(?:N\/A|(({domain}[^"@\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))$"""
  """exa_json_path=$..email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.time,exa_field_name=time"""
  """exa_json_path=$.event_type,exa_field_name=operation"""
  """exa_json_path=$.event_type_description,exa_field_name=additional_info"""
  """exa_json_path=$.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.info_dict.doc_title,exa_field_name=object"""
  """exa_json_path=$..recipient_email,exa_field_name=resource"""
]
ParserVersion = "v1.0.0"


}
```