#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-lock-success-4740-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4740</eventid>"
      "a user account was locked out"
    ]
    Fields = [
      "(?i)({event_name}A user account was locked out)"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)Subject:[^=]+?Account Name:\\s*([\\\\t]*)({src_user}[^:]+?)\\s*([\\\\t]*)Account Domain:\\s*(?=\\w|([\\\\t]*))({src_domain}[^:]+?)\\s*([\\\\t]*)Logon ID:\\s*({login_id}[^:]+?)\\s*Account That Was"
      "(?i)Account That Was Locked Out:\\s*([\\\\t]*)Security ID:\\s*([\\\\t]*)({user_sid}[^:]+?)\\s*([\\\\t]*)Account Name:\\s*([\\\\t]*)({user}[^:]+?)\\s*Additional"
      "(?i)<Data Name ='TargetUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='TargetSid'>({user_sid}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>({src_user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='TargetDomainName'>(?:\\\\+)?({src_host}[^<=\\s]+)(<|\\s)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```