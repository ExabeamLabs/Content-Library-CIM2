#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4776-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""__li_source_path="""
"""attempted to validate the credentials for an account"""
"""eventid="4776""""
]
Fields = [
"""({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
"""__li_source_path="({host}[^"]+)""""
"""Source Workstation:\s*(\\+)?(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(?:(?!NULL)({src_host}[^\s]+)))?(:\d+)?\s*Error Code:"""
"""({event_code}4776)"""
"""Logon (?:a|A)ccount:\s+({user}[^@]+?)(?:@({domain}[^\s.]+)[^\s]*)?\s+Source Workstation"""
"""Error Code:\s+({result_code}[\w\-]+)"""
]
DupFields = ["host->dest_nost"]
ParserVersion = "v1.0.0"


}
```