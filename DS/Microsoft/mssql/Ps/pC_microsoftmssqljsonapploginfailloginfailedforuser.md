#### Parser Content
```Java
{
Name = "microsoft-mssql-json-app-login-fail-loginfailedforuser"
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""source_name":"MSSQLSERVER""""
"""Login failed for user"""
]
Fields = [
""""@timestamp"\s*:\s*\"({time}[^\"]+)\""""
""""computer_name"\s*:\s*\"({host}[\w\-.]+?)\""""
""""source_name\":"({app}[^\"]+)\""""
""""(param1|user)"\s*:\s*\"({user}[\w\.\-]{1,40}\$?)\""""
""""message":\".*?({failure_reason}because[^.]+)\."""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```