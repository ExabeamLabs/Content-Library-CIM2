#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4698-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [
      "4698"
      "a scheduled task was created"
    ]
    Fields = [
      "(?i)EventTime\\\":\\\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)\\\""
      "(?i)({time}\\d\\d\\/\\d\\d\\/\\d\\d\\d\\d \\d\\d:\\d\\d:\\d\\d (am|AM|pm|PM))"
      "(?i)({event_code}4698)"
      "(?i)({event_name}A scheduled task was created)"
      "(?i)\\sComputerName =(|({host}.+?))(\\s+\\w+=|\\s*$)"
      "(?i)\\sKeywords=(|({result}.+?))(\\s+\\w+=|\\s*$)"
      "(?i)Security ID:\\s*(|({user_sid}[^:]+?))\\s*Account Name:\\s*(|({user}[^:]+?))\\s*Account Domain:\\s*(|({domain}[^:]+?))\\s*Logon ID:\\s*(|({login_id}[^:]+?))\\s*Task Information:"
      "(?i)Task Name:\\s*(|({task_name}.+?))\\s*Task Content:"
      "(?i)<UserId>(?=\\w)(({account_domain}[^\\\\<]*)\\\\)?({account_name}[^<]+)</UserId>"
      "(?i)<Settings>\\s*({additional_info}.+?)\\s*</Settings>"
      "(?i)<Triggers>\\s*({triggers}.+?)\\s*</Triggers>"
      "(?i)<RunLevel>(?=\\w)({run_level}[^<]+)</RunLevel>"
      "(?i)<LogonType>(?=\\w)({login_type_text}[^<]+)</LogonType>"
      "(?i)<RegistrationInfo>.+?<Author>(?=\\w)({author}[^<]+)</Author>"
      "(?i)<RegistrationInfo>.+?<Description>(?=\\w)({description}[^<]+)</Description>"
      "(?i)<Command>\\\"?({process_path}({process_dir}(?:(\\w+:)?[^:<\\\"]+)?[\\\\\\/])?({process_name}[^<\\\"]+))"
      "(?i)<Arguments>(\\\"+)?({arg}[^<\\\"]+)"
      "(?i)Computer(\\w+)?[\\\"\\s]*(:|=)\\s*\\\"?({host}.+?)(\\\"|\\s)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```