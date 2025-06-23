#### Parser Content
```Java
{
Name = "microsoft-azuread-json-group-member-remove-success-groupmemberremoved"
Conditions = [
"""Microsoft.aadiam"""
"""Remove member from group"""
"""tenantId":""""
]
ParserVersion = "v1.0.0"

o365-file-app-activity.Fields} [
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
  
}
```