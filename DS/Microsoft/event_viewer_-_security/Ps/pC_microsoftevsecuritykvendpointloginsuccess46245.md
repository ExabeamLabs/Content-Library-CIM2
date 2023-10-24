#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4624-5"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="4624""""
]
Fields = [
""""({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
"""Computer="+({host}[^"]+)""""
"""LogonType="+({login_type}\d+)""""
"""AuthenticationPackageName ="+({auth_package}[^"]+)""""
"""LogonProcessName ="+({auth_process}[^"]+)""""
"""EventID="+({event_code}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""TargetUserName ="+({user}[\w\.\-]{1,40}\$?)""""
"""TargetLogonId="+({login_id}[^"]+)""""
"""TargetUserSid="+({user_sid}[^"]+)""""
"""TargetDomainName ="+({domain}[^"]+)""""
"""IpAddress="+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
"""WorkstationName ="+([A-Fa-f:\d.]+|({src_host_windows}[^"]+))""""
"""ProcessName ="(-|({process_path}[^"]+))"""
"""KeyLength="+({key_length}\d+)""""
"""SubjectUserSid="+({subject_sid}[^"]+)""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```