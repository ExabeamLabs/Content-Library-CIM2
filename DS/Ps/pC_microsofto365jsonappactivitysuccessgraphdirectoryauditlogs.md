#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-success-graphdirectoryauditlogs
Conditions = [
  """"src-application-name":"Office 365""""
  """"event-name":"user-suspended""""
  """initiatedBy":"""
  """"src-endpoint":"Graph Directory Audit logs""""
  """"category":"UserManagement""""
]
ParserVersion = "v1.0.0"

o365-file-app-activity.Fields} [
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
  
}
```