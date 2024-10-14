#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4776-4"
Conditions = [
""""event-id":4776"""
""""message":"The computer attempted to validate the credentials for an account"""
""""user":"""
]
ParserVersion = "v1.0.0"

windows-events-wls= {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+).+\sLogType""",
    """EventID="+({event_code}\d+)"""",
    """Opcode.+ProcessName ="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+))({process_name}[^"]+))"""",
    """ServiceName ="+({service_name}[^"]+)"""",
    """ServiceType="+({service_type}[^"]+)"""",
    """ServiceAccount="+({account_name}[^"]+)"""",
    """SubjectUserName ="+(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """SubjectDomainName ="+(-|({domain}[^"]+))"""",
    """SubjectLogonId="+({login_id}[^"]+)"""",
    """ProviderGuid="+({process_guid}[^"]+)"""",
    """CommandLine="+({process_command_line}[^"]+)"""",
    """SubjectUserSid="+({user_sid}[^"]+)"""",
    """SubjectUserName ="+(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """ObjectServer="+({object_server}[^"]+)"""",
    """ProcessId="+({process_id}[^"]+)"""",
    """Computer="+({host}[\w\-.]+)"""",
    """TargetDomainName ="+(-|({dest_domain}[^"]+))"""",
    """TargetUserName ="+(-|({dest_user}[^"]+))"""",
    """TargetLogonId="+({dest_user_sid}[^"]+)"""",
    """TargetUserSid="+({dest_user_sid}[^"]+)"""",
    """ExecutionProcessID="+({process_id}d+)"""",
    """FailureReason="+({failure_reason}[^"]+)"""",
    """WorkstationName ="+(-|({client}[^"]+))"""",
    """MemberName ="+({user_dn}[^"]+)"""",
    """MemberSid="+({account_id}[^"]+)"""",
    """LogonType="+({login_type}\d+)"""",
    """SubStatus="+({result_code}\d+)"""",
    """LogonProcessName ="({auth_process}[^"]+)"""",
    """KeyLength="({key_length}\d+)"""",
    """AuthenticationPackageName ="({auth_package}[^"]+)"""",
    """IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
    
}
```