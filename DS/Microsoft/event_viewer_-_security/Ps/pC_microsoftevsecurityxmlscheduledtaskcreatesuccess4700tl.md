#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4700-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4700</eventid>"
      "<data name='subjectusername'>"
      "<message>a scheduled task was enabled"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)({event_code}4700)"
      "(?i)({event_name}A scheduled task was enabled)"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"
      "(?i)<Data Name ='TaskName'>({task_name}[^<]+)<"
      "(?i)<Data Name ='TaskContent'>({additional_info}[^<]+)<"
    ]
    ParserVersion = "v1.0.0"
  

}
```