#### Parser Content
```Java
{
Name = "microsoft-azuread-json-user-password-reset-fail-changepassword"
Conditions = [
"""Microsoft.aadiam"""
"""Change user password"""
"""tenantId":""""
]
ExtractionType = json
ParserVersion = "v1.0.0"

o365-file-app-activity.Fields} [
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
  
}
```