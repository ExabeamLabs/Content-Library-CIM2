#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624-6"
Conditions = [
  """subject.logon_id"""
  """EventID"""
  """4624"""
]
ParserVersion = "v1.0.0"

windows-events-2.Fields}[
    """SubjectUserName\\?"+:\\?"({src_user}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"({src_domain}[^\\]+)\\?"""",
    """SubjectLogonId\\?"+:\\?"({login_id}[^\\]+)\\?"""",
    """TargetSid\\?"+:\\?"({user_sid}[^\\]+)\\?"""",
    """TargetUserName\\?"+:\\?"({user}[^\\]+)\\?"""",
    """TargetDomainName\\?"+:\\?"({src_host}[^\s\\]+)\\?""""
  ]
  DupFields=[ "host->dest_host", "src_domain->domain" 
}
```