#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-4728"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""A member was added to a security-enabled"""
"""event_id\":4728"""
"""computer_name"""
]
Fields = [
"""@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""(?:winlog\.)?computer_name\\?"+:\\?"+({host}[^\\]+)"""
"""SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^\\]+))\\?""""
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
"""A member was added to a security-enabled ({group_type}\w+) group"""
"""MemberName\\?"+:\\?"+(-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-\\]+?)))\\?""""
"""MemberSid\\?"+:\\?"+({account_id}[^\\]+)\\?""""
"""TargetSid\\?"+:\\?"+({group_id}[^\\]+)\\?""""
"""TargetUserName\\?"+:\\?"+({group_name}[^\\]+)\\?""""
"""TargetDomainName\\?"+:\\?"+({group_domain}[^\\]+)\\?""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```