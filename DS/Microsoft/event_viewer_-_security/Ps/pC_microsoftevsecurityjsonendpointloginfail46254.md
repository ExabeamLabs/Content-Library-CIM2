#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-4625-4"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """"FailureReason\""""
    """"EventID\":4625"""
    """An account failed to log on"""
  ]
  Fields = [
    """({event_name}An account failed to log on)"""
    """"EventTime\\*":\\*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime\\*":\s*({time}\d+)"""
    """"timestamp\\*":\s*({time}\d+)"""
    """"(Hostname|MachineName)\\*":\\*"({host}[\w\-.]*)"""
    """({event_code}4625)"""
    """"SubjectUserSid\\*":\\*"({user_sid}[^\\"]+)"""
    """"SubjectUserName\\*":\\*"(?:-|({src_user}[^"\\]+))"""
    """"SubjectDomainName\\*":\\*"(?:-|({src_domain}[^"\\]+))"""
    """"LogonType\\*":\\*"({login_type}\d+)"""
    """"TargetUserName\\?":\\?"\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^'\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
    """"TargetDomainName\\*":\\*"({domain}[^."\\]+)"""
    """"SubStatus\\*":\\*"({result_code}[^"\\]+)"""
    """"WorkstationName\\*":\\*"({src_host_windows}[^"\\]+)"""
    """"LogonProcessName\\*":\\*"({auth_process}[^."\\]+?)\s*\\*""""
    """"AuthenticationPackageName\\*":\\*"({auth_package}[^"\\]+)"""
    """"IpAddress\\*":\\*"(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """"KeyLength\\*":\\*"({key_length}\d+)"""
    """"SubjectUserSid\\*":\\*"({subject_sid}[^"\\]+)"""
    """Subject(:|=).+?Account Name(:|=)\s*((\\)*(\\r|\\t|\\n))*(-|({src_user}[^\s@]+?))[\s;]*((\\)*(\\r|\\t|\\n))*Account Domain(:|=)"""
    """Subject(:|=).+?Account Domain(:|=)\s*((\\)*(\\r|\\t|\\n))*(-|({src_domain}[^:;]+?))[\s;]*((\\)*(\\r|\\t|\\n))*Logon ID(:|=)"""
  ]
  DupFields = [
    "host->dest_host"
    "result_code->failure_code",
    "src_host_windows->src_host"
  ]


}
```