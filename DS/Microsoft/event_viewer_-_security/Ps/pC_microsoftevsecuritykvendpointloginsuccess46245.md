#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4624-5"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
"""LogType="WLS""""
"""EventID="4624""""
]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
""""({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
"""Computer="+({dest_host}({host}[^"]+))""""
"""LogonType="+({login_type}\d+)""""
"""AuthenticationPackageName ="+({auth_package}[^"]+)""""
"""LogonProcessName ="+({auth_process}[^"]+)""""
"""EventID="+({event_code}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""TargetUserName ="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""TargetLogonId="+({dest_login_id}({login_id}[^"]+))""""
"""TargetUserSid="+({dest_user_sid}({user_sid}[^"]+))""""
"""TargetDomainName ="+({dest_domain}({domain}[^"]+))""""
"""IpAddress="+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
"""WorkstationName ="+([A-Fa-f:\d.]+|({src_host_windows}({src_host}[^"]+)))""""
"""ProcessName ="(-|({process_path}[^"]+))"""
"""KeyLength="+({key_length}\d+)""""
"""SubjectUserSid="+({subject_sid}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```