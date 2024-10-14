#### Parser Content
```Java
{
Name = "microsoft-mssql-json-app-login-fail-loginfailedforuser"
Vendor = "Microsoft"
Product = "MSSQL"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""source_name":"MSSQLSERVER""""
"""Login failed for user"""
]
Fields = [
"""exa_regex="@timestamp"\s*:\s*\"({time}[^\"]+)\"""",
"""exa_json_path=$.computer_name,exa_field_name=host""",
"""exa_json_path=$.source_name,exa_field_name=app""",
"""exa_json_path=$.event_data.param1,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
"""exa_json_path=$.user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
"""exa_json_path=$.message,exa_regex=.*?({failure_reason}because[^.]+)\."""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```