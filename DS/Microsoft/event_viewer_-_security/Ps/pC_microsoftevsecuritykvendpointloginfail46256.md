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
"""Computer="+({host}[^"]+)""""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""EventID="+({event_code}[^"]+)""""
"""IpAddress="+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
"""LogonProcessName ="+({auth_process}[^"]+)""""
"""LogonType="+({login_type}\d+)""""
"""AuthenticationPackageName ="+({auth_package}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""SubStatus="+({result_code}[^"]+)""""
"""SubjectUserName ="+(?=\w)({src_user}[^"]+)""""
"""SubjectDomainName ="+(?=\w)({src_domain}[^"]+)""""
"""TargetDomainName ="(?:-|({domain}[^"]+))"""
"""TargetUserName ="+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\s]+))?""""
"""TargetUserSid="+({user_sid}[^"]+)""""
"""WorkstationName ="+(-|({src_host_windows}[^"]+))""""
"""FailureReason="+({failure_reason}[^"]+)""""
]
DupFields = [ "host->dest_host", "src_host_windows->src_host", "user_sid->dest_user_sid", "domain->dest_domain", "user->dest_user" ]
ParserVersion = "v1.0.0"


}
```