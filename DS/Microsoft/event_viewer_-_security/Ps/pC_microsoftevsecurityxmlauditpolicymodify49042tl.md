#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-audit-policy-modify-4904-2-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "an attempt was made to register a security event source"
      "4904"
    ]
    Fields = [
      "(?i)({event_name}An attempt was made to register a security event source)"
      "(?i)<Computer>(::ffff:)?({host}[^<]+)</Computer>"
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+\\.\\d+)"
      "(?i)(?i)\\w+\\s*\\d+\\s\\d+:\\d+:\\d+\\s+(::ffff:)?(am|pm|({host}[\\w\\-.]+))"
      "(?i)({event_code}4904)"
      "(?i)\\sAccount Name:\\s*(|-|({user}.+?))\\s*Account Domain:\\s*(|-|({domain}.+?))\\s*Logon ID:\\s*(|-|({login_id}.+?))\\s*Process:"
      "(?i)\\sProcess ID:\\s*(|-|({process_id}.+?))\\s*Process Name:\\s*(|-|({process_path}({process_dir}.*?)({process_name}[^\\\\\\/]+?)))\\s*Event Source:"
      "(?i)(?i)\\w+\\s*\\d+\\s*\\d+:\\d+:\\d+\\s+(::ffff:)?(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?|(am|pm|({dest_host}[\\w\\-.]+)))"
    ]
    DupFields = [
      "host-> dest_host"
    ]
  

}
```