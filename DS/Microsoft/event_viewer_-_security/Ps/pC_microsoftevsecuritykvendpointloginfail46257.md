#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4625-7"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
"""Exabeam Windows 4625"""
"""summary_windows_4625_data="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
"""({event_code}4625)"""
"""summary_windows_4625_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::(-|({host}[^:::]+))?:::(-|({src_user}[^:::]+))?:::(-|({src_domain}[^:::]+))?:::(-|({login_type}\d+))?:::(-|({user_sid}[^:::]+))?:::(-|({user}[^:::]+))?:::(-|({domain}[^:::]+))?:::(-|({result_code}[^:::]+))?:::(-|({src_host_windows}[^:::]+))?:::(-|({src_host}[^:::]+))?:::(-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?:::(-|({auth_process}[^:::]+))?:::(-|({auth_package}[^:::]+))?:::(-|({failure_reason}.+?))?""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```