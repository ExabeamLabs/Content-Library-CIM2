#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-modify-taskupdated-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "a scheduled task was updated"
      "<userid>"
      "<command>"
      "<arguments>"
    ]
    Fields = [
      "(?i)({event_name}A scheduled task was updated)"
      "(?i)Account Name:\\s*({user}.+?)\\s*Account Domain:\\s*({domain}.+?)\\s*Logon ID:\\s*({login_id}.+?)\\s*Task Information:"
      "(?i)Task Name:\\s*({task_name}.+?)\\s*Task New"
      "(?i)<UserId>({user_sid}[^<]+?)</UserId>"
      "(?i)<RunLevel>({run_level}[^<]+?)</RunLevel>"
      "(?i)<Triggers>\\s*({triggers}.+?)\\s*</Triggers>"
      "(?i)<Command>({process_path}({process_dir}(?:(\\w+:)?[^:<\"]+?)?[\\\\\\/]+)?({process_name}[^<\"\\\\\\/]+?))</Command>"
      "(?i)<Arguments>({arg}[^<]+?)</Arguments>"
    ]
  

}
```