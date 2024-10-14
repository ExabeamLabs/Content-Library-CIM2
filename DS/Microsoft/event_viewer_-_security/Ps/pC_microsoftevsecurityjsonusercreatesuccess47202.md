#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-create-success-4720-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""A user account was created"""
"""event_id":4720"""
"""computer_name"""
]
Fields = [
"""@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""(?:winlog\.)?computer_name\\?"+:\\?"+({host}[^\\]+)"""
"""SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
"""SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?""""
"""SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?""""
"""SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
"""event_id\\?"+:({event_code}\d+)"""
"""ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?""""
"""WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}[^\s\\]+))\\?""""
"""Status\\?"+:\\?"+({result_code}[^\\]+)\\?""""
"""ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?""""
"""LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?""""
"""AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
"""({event_name}A user account was created)"""
"""TargetSid\\?"+:\\?"+({account_id}[^"\\]+)"""
"""TargetUserName\\?"+:\\?"+({account_name}[^"\\]+)"""
"""TargetDomainName\\?"+:\\?"+({account_domain}[^"\\]+)"""
"""(\\+t)+'({user_type}[^']+)'\s*-\s*Enabled"""
]
DupFields = [
"account_name->dest_user",
"src_host_windows->src_host",
"account_domain->dest_domain"
]
ParserVersion = "v1.0.0"


}
```