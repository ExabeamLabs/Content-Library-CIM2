#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-login-success-33205
Conditions = [
  """EventCode=33205"""
  """action_id:LGIS"""
]
ParserVersion = "v1.0.0"

SSSZ"
    Fields = [
      """exa_regex="@timestamp"\s*:\s*"({time}[^"]+)"""",
      """exa_json_path=$.winlog.computer_name,exa_field_name=host""",
      """exa_json_path=$.message,exa_regex=CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_regex=({app}MSSQLSERVER)""",
      """exa_json_path=$.message,exa_field_name=additional_info"""
    
}
```