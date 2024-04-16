#### Parser Content
```Java
{
Name = "netdoc-n-json-file-activity-success"
Product = "NetDocs"
Vendor = "NetDocs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [
"""memberType": """
"""storageObject":"""
"""cabinet": """
]
Fields = [
  """exa_json_path=$..host,exa_field_name=host"""
  """exa_json_path=$..host,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$..date,exa_field_name=time"""
  """exa_json_path=$..user.name,exa_field_name=full_name"""
  """exa_json_path=$..cabinet.id,exa_field_name=user_id"""
  """exa_json_path=$..user.memberType,exa_field_name=object"""
  """exa_json_path=$..size,exa_field_name=bytes"""
  """exa_json_path=$..fileExtension,exa_field_name=file_ext"""
  """exa_json_path=$..cabinet.id,exa_field_name=dest_host"""
  """exa_json_path=$.activity.name,exa_field_name=operation"""
  """exa_json_path=$..CorpMatter,exa_field_name=corp_matter"""
  """exa_json_path=$..CorpClient,exa_field_name=corp_client"""
  """exa_json_path=$..cabinet.name,exa_field_name=cabinet_name"""
  """exa_json_path=$..storageObject.name,exa_field_name=src_file_name"""
  """exa_json_path=$..docId,exa_field_name=doc_id"""
  """exa_json_path=$..access,exa_field_name=additional_info"""
  """exa_regex=({app}netdocs)"""
]
DupFields = [
"operation->access"
]
ParserVersion = "v1.0.0"


}
```