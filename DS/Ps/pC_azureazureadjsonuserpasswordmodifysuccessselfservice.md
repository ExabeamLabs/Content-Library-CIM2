#### Parser Content
```Java
{
Name = "azure-azuread-json-user-password-modify-success-selfservice"
ExtractionType = json
Conditions = [
"""Microsoft.aadiam"""
"""Self-service password reset"""
"""tenantId":""""
]
ParserVersion = "v1.0.0"

o365-file-app-activity.Fields} [
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
  
}
```