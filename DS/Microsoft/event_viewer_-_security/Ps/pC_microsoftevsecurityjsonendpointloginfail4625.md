#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-4625"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """"FailureReason":"""
    """"EventID":4625"""
    """An account failed to log on"""
  ]
  Fields = [
    """({event_name}An account failed to log on)"""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime":\s*({time}\d+)"""
    """"timestamp":\s*({time}\d+)"""
    """"(Hostname|MachineName)":"({host}[^"]*)"""
    """({event_code}4625)"""
    """"SubjectUserSid":"({user_sid}[^"]+)"""
    """"SubjectUserName":"(?:-|({src_user}[^"]+))"""
    """"SubjectDomainName":"(?:-|({src_domain}[^"]+))"""
    """"LogonType":"({login_type}\d+)"""
    """"TargetUserName":"({user}[^"]+)"""
    """"TargetDomainName":"({domain}[^."]+)"""
    """"SubStatus":"({result_code}[^"]+)"""
    """"WorkstationName":"({src_host_windows}[^"]+)"""
    """"LogonProcessName":"({auth_process}[^."]+?)\s*""""
    """"AuthenticationPackageName":"({auth_package}[^"]+)"""
    """"IpAddress":"(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """"KeyLength":"({key_length}\d+)"""
    """"SubjectUserSid":"({subject_sid}[^"]+)"""
    """Subject(:|=).+?Account Name(:|=)\s*(-|({src_user}[^\s@]+?))[\s;]*Account Domain(:|=)"""
    """Subject(:|=).+?Account Domain(:|=)\s*(-|({src_domain}[^:;]+?))[\s;]*Logon ID(:|=)"""
  ]
  DupFields = [
    "host->dest_host"
    "result_code->failure_code"
  ]


}
```