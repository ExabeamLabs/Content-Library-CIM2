#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4698-2-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "epoch_sec"
    Conditions = [
      "eventid=4698"
      "a scheduled task was created"
    ]
    Fields = [
      "(?i)\\WComputer=({host}[\\w\\.\\-]+)"
      "(?i)\\WEventID=({event_code}\\d+)"
      "(?i)\\WTimeGenerated=({time}\\d{10})"
      "(?i)\\sAccount Name:\\s*(|({user}.+?))\\s*Account Domain:\\s*(|({domain}.+?))\\s*Logon ID:\\s*(|({login_id}.+?))\\s*Task Information:"
      "(?i)\\sTask Name:\\s*(|(?=[\\\\\\w])({task_name}.+?))\\s*Task Content:"
      "(?i)<UserId>(?=\\w)(({account_domain}[^\\\\<]*)\\\\)?({account_name}[^<]+)</UserId>"
      "(?i)<RunLevel>(?=\\w)({run_level}[^<]+)</RunLevel>"
      "(?i)<RegistrationInfo>.+?<Description>(?=\\w)({description}[^<]+)</Description>"
      "(?i)<Command>\\\"?({process_path}({process_dir}(?:(\\w+:)?[^:<\\\"]+)?[\\\\\\/])?({process_name}[^<\\\"]+))"
      "(?i)<Arguments>(\\\"+)?({arg}[^<\\\"]+)"
      "(?i)({event_name}a scheduled task was created)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```