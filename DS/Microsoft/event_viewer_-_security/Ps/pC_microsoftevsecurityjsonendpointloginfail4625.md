#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-4625"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
    """"FailureReason":"""
    """"EventID":"""
    """4625"""
    """"LogonProcessName":""""
    """"AuthenticationPackageName":""""
  ]
  Fields = [
    """({event_name}An account failed to log on)"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"EventTime\\?":\\?"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"EventReceivedTime\\?":\s*({time}\d+)"""
    """"timestamp\\?":\s*({time}\d+)"""
    """"(Hostname|MachineName)\\?":\\?"({host}[\w\-.]*)"""
    """({event_code}4625)"""
    """"SubjectUserSid\\?":\\?"({user_sid}[^\\"]+)"""
    """"SubjectUserName\\?":\\?"(?:-|({src_user}[^"\\]+))"""
    """"SubjectDomainName\\?":\\?"(?:-|({src_domain}[^"\\]+))"""
    """"LogonType\\?":\\?"({login_type}\d+)"""
    """"(TargetUserName|AccountName)":"\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"TargetDomainName\\?":\\?"({domain}[^."\\]+)"""
    """"SubStatus\\?":\\?"({result_code}[^"\\]+)"""
    """"WorkstationName\\?":\\?"({src_host_windows}[^"\\]+)"""
    """"LogonProcessName\\?":\\?"({auth_process}[^."\\]+?)\s*\\?""""
    """"AuthenticationPackageName\\?":\\?"({auth_package}[^"\\]+)"""
    """"IpAddress\\?":\\?"(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """"KeyLength\\?":\\?"({key_length}\d+)"""
    """"SubjectUserSid\\?":\\?"({subject_sid}[^"\\]+)"""
    """Subject(:|=).+?Account Name(:|=)\s*((\\)*(\\r|\\t|\\n))*(-|({src_user}[^\s@]+?))[\s;]*((\\)*(\\r|\\t|\\n))*Account Domain(:|=)"""
    """Subject(:|=).+?Account Domain(:|=)\s*((\\)*(\\r|\\t|\\n))*(-|({src_domain}[^:;]+?))[\s;]*((\\)*(\\r|\\t|\\n))*Logon ID(:|=)"""
    """Account Name:((?-i)\\+[rnt])*(-|({account}.+?))((?-i)\\+[rnt])*Account Domain"""
    """"FailureReason":"({failure_reason}[^"]+)""""
    """exa_regex=({event_name}An account failed to log on)"""
    """exa_regex="TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_regex="EventTime\\?":\\?"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """exa_regex="EventReceivedTime\\?":\s*({time}\d+)"""
    """exa_regex="timestamp\\?":\s*({time}\d+)"""
    """exa_regex="(Hostname|MachineName)\\?":\\?"({host}[\w\-.]*)"""
    """exa_regex=({event_code}4625)"""
    """exa_regex="SubjectUserSid\\?":\\?"({user_sid}[^\\"]+)"""
    """exa_regex="SubjectUserName\\?":\\?"(?:-|({src_user}[^"\\]+))"""
    """exa_regex="SubjectDomainName\\?":\\?"(?:-|({src_domain}[^"\\]+))"""
    """exa_regex="LogonType\\?":\\?"({login_type}\d+)"""
    """exa_regex="(TargetUserName|AccountName)":"\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """exa_regex="TargetDomainName\\?":\\?"({domain}[^."\\]+)"""
    """exa_regex="SubStatus\\?":\\?"({result_code}[^"\\]+)"""
    """exa_regex="WorkstationName\\?":\\?"({src_host_windows}[^"\\]+)"""
    """exa_regex="LogonProcessName\\?":\\?"({auth_process}[^."\\]+?)\s*\\?""""
    """exa_regex="AuthenticationPackageName\\?":\\?"({auth_package}[^"\\]+)"""
    """exa_regex="IpAddress\\?":\\?"(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """exa_regex="KeyLength\\?":\\?"({key_length}\d+)"""
    """exa_regex="SubjectUserSid\\?":\\?"({subject_sid}[^"\\]+)"""
    """exa_regex=Subject(:|=).+?Account Name(:|=)\s*((\\)*(\\r|\\t|\\n))*(-|({src_user}[^\s@]+?))[\s;]*((\\)*(\\r|\\t|\\n))*Account Domain(:|=)"""
    """exa_regex=Subject(:|=).+?Account Domain(:|=)\s*((\\)*(\\r|\\t|\\n))*(-|({src_domain}[^:;]+?))[\s;]*((\\)*(\\r|\\t|\\n))*Logon ID(:|=)"""
    """exa_regex=Account Name:((?-i)\\+[rnt])*(-|({account}.+?))((?-i)\\+[rnt])*Account Domain"""
    """exa_regex="FailureReason":"({failure_reason}[^"]+)""""
  ]
  DupFields = [ "host->dest_host", "result_code->failure_code", "email_address->dest_email_address", "user->dest_user", "domain->dest_domain" ]


}
```