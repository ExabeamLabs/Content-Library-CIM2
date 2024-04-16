#### Parser Content
```Java
{
Name = microsoft-mssql-json-app-login-fail-loginfailedforuser-1
  Vendor = Microsoft
  Product = MSSQL
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"provider_name":"MSSQLSERVER"""", """Login failed for user""" ]
  Fields = [
    """exa_regex="@timestamp"\s*:\s*"({time}[^"]+)"""",
    """exa_json_path=$.winlog.computer_name,exa_field_name=host""",
    """exa_json_path=$.winlog.event_data.param3,exa_regex=\[CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """exa_regex=({app}MSSQLSERVER)""",
    """exa_json_path=$.event.outcome,exa_field_name=result""",
    """exa_json_path=$.message,exa_regex=Reason:\s*({failure_reason}[^"\.\[]+)""",
    """exa_json_path=$.message,exa_regex=({event_name}Login failed for user) '(({domain}[^\\:']+?)\\+)?({user}[\w\.\-]{1,40}\$?)'""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```