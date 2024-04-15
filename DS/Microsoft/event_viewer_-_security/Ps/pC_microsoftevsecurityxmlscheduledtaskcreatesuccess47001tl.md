#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4700-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "4700"
      "a scheduled task was enabled"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+?)</Computer>"
      "(?i)({event_code}4700)"
      "(?i)({event_name}A scheduled task was enabled)"
      "(?i)\\sAccount Name:\\s*(|({user}[^:]+?))\\s*Account Domain:\\s*(|({domain}[^:]+?))\\s*Logon ID:\\s*(|({login_id}[^:]+?))\\s*Task Information:"
      "(?i)Task Name:\\s*({task_name}[^:]+?)\\s*Task Content:"
      "(?i)Task Content:\\s*({additional_info}[^<]+?)\\s*<"
    ]
    ParserVersion = "v1.0.0"
  

}
```