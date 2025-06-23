#### Parser Content
```Java
{
Name = microsoft-azuread-sk4-user-password-modify-success-changepassword
Conditions = [
  """"Resource":"Microsoft.aadiam""""
  """"OperationName":"Change password (self-service)""""
  """"TenantId":""""
  """"Type":"AuditLogs""""
]
ParserVersion = "v1.0.0"

o365-file-app-activity.Fields} [
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
  
}
```