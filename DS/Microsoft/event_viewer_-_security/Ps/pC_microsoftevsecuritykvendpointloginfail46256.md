#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4625-6"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="4625""""
]
Fields = [
"""Computer="+({dest_host}({host}[^"]+))""""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""EventID="+({event_code}[^"]+)""""
"""IpAddress="+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
"""LogonProcessName ="+({auth_process}[^"]+)""""
"""LogonType="+({login_type}\d+)""""
"""AuthenticationPackageName ="+({auth_package}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""SubStatus="+({result_code}[^"]+)""""
"""SubjectUserName ="+(?=\w)({src_user}[^"]+)""""
"""SubjectDomainName ="+(?=\w)({src_domain}[^"]+)""""
"""TargetDomainName ="(?:-|({dest_domain}({domain}[^"]+)))"""
"""TargetUserName ="+(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\s]+)))?""""
"""TargetUserSid="+({dest_user_sid}({user_sid}[^"]+))""""
"""WorkstationName ="+(-|({src_host_windows}({src_host}[\w\-\.]+)))""""
"""FailureReason="+({failure_reason}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```