#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-4688-5
  Conditions = [ """LogType="WLS"""", """EventID="4688"""" ]
  ParserVersion = "v1.0.0"

windows-events-wls= {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+).+\sLogType""",
    """EventID="+({event_code}\d+)"""",
    """Opcode.+ProcessName ="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+))({process_name}[^"]+))"""",
    """ServiceName ="+({service_name}[^"]+)"""",
    """ServiceType="+({service_type}[^"]+)"""",
    """ServiceAccount="+({account_name}[^"]+)"""",
    """SubjectUserName ="+(-|({user}[^"]+))"""",
    """SubjectDomainName ="+(-|({domain}[^"]+))"""",
    """SubjectLogonId="+({login_id}[^"]+)"""",
    """ProviderGuid="+({process_guid}[^"]+)"""",
    """CommandLine="+({process_command_line}[^"]+)"""",
    """SubjectUserSid="+({user_sid}[^"]+)"""",
    """SubjectUserName ="+(-|({user}[^"]+))"""",
    """ObjectServer="+({object_server}[^"]+)"""",
    """ProcessId="+({process_id}[^"]+)"""",
    """Computer="+({dest_host}[^"]+)"""",
    """TargetDomainName ="+(-|({dest_domain}[^"]+))"""",
    """TargetUserName ="+(-|({dest_user}[^"]+))"""",
    """TargetLogonId="+({dest_user_sid}[^"]+)"""",
    """TargetUserSid="+({dest_user_sid}[^"]+)"""",
    """ExecutionProcessID="+({process_id}d+)"""",
    """FailureReason="+({failure_reason}[^"]+)"""",
    """WorkstationName ="+(-|({workstation}[^"]+))"""",
    """MemberName ="+({user_dn}[^"]+)"""",
    """MemberSid="+({account_id}[^"]+)"""",
    """LogonType="+({login_type}\d+)"""",
    """SubStatus="+({http_response_code}\d+)"""",
    """LogonProcessName ="({auth_process}[^"]+)"""",
    """KeyLength="({key_length}\d+)"""",
    """AuthenticationPackageName ="({auth_package}[^"]+)"""",
    """IpAddress="(-|({src_ip}[a-fA-F\d:.]+))""""
    ]
    DupFields = [ "dest_host->host" 
}
```