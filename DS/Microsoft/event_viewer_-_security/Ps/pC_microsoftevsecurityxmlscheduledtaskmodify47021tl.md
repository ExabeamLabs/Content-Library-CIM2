#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-modify-4702-1-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4702<"
      "a scheduled task was updated"
      "&lt;settings&gt;"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{9}Z)"
      "(?i)({event_code}4702)"
      "(?i)({event_name}A scheduled task was updated)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Keywords>({result}.+?)</Keywords>"
      "(?i)Security ID:\\s*({user_sid}.+?)\\s*Account Name:\\s*({user}.+?)\\s*Account Domain:\\s*({domain}.+?)\\s*Logon ID:\\s*({login_id}.+?)\\s*Task Information:"
      "(?i)Task Name:\\s*({task_name}.+?)\\s*Task New"
      "(?i)&lt;UserId&gt;(({account_domain}[^\\\\&]*)\\\\)?({account_name}[^&]+)&lt;/UserId&gt;"
      "(?i)&lt;Triggers&gt;\\s*({triggers}.+?)\\s*&lt;/Triggers&gt;"
      "(?i)&lt;RunLevel&gt;({run_level}[^&]+)&lt;/RunLevel&gt;"
      "(?i)&lt;Author&gt;(?=\\w)({author}.+?)&lt;/Author&gt;"
      "(?i)&lt;Description&gt;(?=\\w)({description}.+?)&lt;/Description&gt;"
      "(?i)&lt;Command&gt;\"?({process_path}({process_dir}(?:(\\w+:)?[^:&\"]+?)?[\\\\\\/]+)?({process_name}[^&\"\\\\\\/]+?))&lt;/Command&gt;"
      "(?i)&lt;Arguments&gt;({arg}.+?)&lt;/Arguments&gt;"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```