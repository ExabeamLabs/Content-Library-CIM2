#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-login-fail-33205
Conditions = [
  """EventCode=33205"""
  """action_id:LGIF"""
]
ParserVersion = "v1.0.0"

SSSZ"
    Fields = [
      """"@timestamp"\s*:\s*"({time}[^"]+)"""",
      """"computer_name"\s*:\s*"({host}[\w.-]+?)"""",
      """CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """({app}MSSQLSERVER)""",
      """"message":"({additional_info}[^"]+)"""
    
}
```