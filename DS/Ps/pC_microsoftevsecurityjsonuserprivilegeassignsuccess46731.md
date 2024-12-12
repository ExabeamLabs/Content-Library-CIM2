#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4673-1"
Conditions = [ """"EventID":"4673"""", """A privileged service was called""" ]
ExtractionType = json
ParserVersion = "v1.0.0"

windows-events-2.Fields}[
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host}({src_host_windows}[^\s\\]+)))\\?"""",
    """SubjectUserName\\?"+:\\?"({src_user}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"({src_domain}[^\\]+)\\?"""",
    """SubjectLogonId\\?"+:\\?"({login_id}[^\\]+)\\?"""",
    """TargetSid\\?"+:\\?"({user_sid}[^\\]+)\\?"""",
    """TargetUserName\\?"+:\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"""",
    """TargetDomainName\\?"+:\\?"({src_host}[^\s\\]+)\\?""""
  ]
  DupFields=[ "src_domain->domain" 
}
```