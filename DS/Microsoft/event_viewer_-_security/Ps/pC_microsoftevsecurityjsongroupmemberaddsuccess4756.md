#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-group-member-add-success-4756
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4756""", """Microsoft-Windows-Security-Auditing""", """"Channel":"Security"""", """"MemberName":"""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
    """"EventID":({event_code}4756)"""
    """"Hostname":"({host}[\w\-.]+)""""
    """"MemberName":"({user_dn}(cn)=({account_name}[^,]+),({user_ou}OU.+?DC=[\w-]+))""""
    """"MemberSid":"(({dest_user_sid}S-\d+-[^:\s"]+)|({account_domain}[^\\\s"]+)\\+({account_name}[^\s"]+))""""
    """"TargetUserName":"(?=\w)({group_name}[^"]+)""""
    """"TargetDomainName":"(?=\w)({group_domain}[^"]+)""""
    """"TargetSid":"({group_id}[^"]+)""""
    """"SubjectUserSid":"({user_sid}[^"]+)""""
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"SubjectDomainName":"({domain}[^"]+)""""
    """"SubjectLogonId":"({login_id}[^"]+)""""
    """"SourceName":"({provider_name}[^"]+)""""
    """"ProcessID":({process_id}\d+),"""
    """"Category":"({category}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```