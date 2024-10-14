#### Parser Content
```Java
{
Name = "microsoft-o365-cef-file-read-success-memberadded"
Conditions = [
  """CEF:"""
  """|Microsoft Teams|"""
  """|MemberAdded|"""
]
ParserVersion = "v1.0.0"

microsoft-azure-endpoint-json.Fields} [
    """exa_json_path=$.Uri,exa_field_name=file_path""",
    """exa_json_path=$.AccountName,exa_field_name=storage_account""",
    """exa_json_path=$.['_ResourceId'],exa_field_name=resource"""
  
}
```