#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-password-reset-success-4724-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""An attempt was made to reset an account's password"""
"""computer_name"""
"""event_id\":4724"""
]
Fields = [
"""@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}({host}[^\\]+))"""
"""SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?""""
"""SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?""""
"""SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\]+)))\\?""""
"""SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
"""event_id\\?"+:({event_code}\d+)"""
"""ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?""""
"""WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?""""
"""Status\\?"+:\\?"+({result_code}[^\\]+)\\?""""
"""ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?""""
"""LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?""""
"""AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
"""({event_name}An attempt was made to reset an account's password)"""
"""TargetUserName\\?"+:\\?"({dest_user}[^\\]+)\\?""""
"""TargetDomainName\\?"+:\\?"({dest_domain}[^\s\\]+)\\?""""
""""TargetSid\\?"+:\\?"({dest_user_sid}[^\\]+)"""
]
ParserVersion = "v1.0.0"


}
```