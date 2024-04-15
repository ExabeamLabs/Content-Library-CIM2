#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-activity-success-4662-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>4662<"
      "オブジェクトに対して操作が実行されました。"
    ]
    Fields = [
      "(?i)({event_name}オブジェクトに対して操作が実行されました。)"
      "(?i)({event_code}4662)"
      "(?i)({time}\\d\\d/\\d\\d/\\d\\d\\d\\d \\d\\d:\\d\\d:\\d\\d (AM|PM|am|pm))"
      "(?i)({time}\\w+ \\d\\d \\d\\d:\\d\\d:\\d\\d \\d\\d\\d\\d)\\s+"
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'/>"
      "(?i)Computer(Name)?\\s*\\\\*\"?(=|:|>)\\s*\"*({host}[\\w\\.-]+)(\\s|,|\"|</Computer>|$)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)'SubjectUserSid'>({user_sid}[^\"\\s<]+)<"
      "(?i)'SubjectUserName'>({user}[^\"\\s<]+)<"
      "(?i)'SubjectDomainName'>({domain}[^\"\\s<]+)<"
      "(?i)'SubjectLogonId'>({login_id}[^\"\\s<]+)<"
      "(?i)'ObjectServer'>({object_class}[^<]+)<"
      "(?i)'ObjectType'>\\%?\\{?({object_type}[^<>\\{\\}]+)"
      "(?i)'ObjectName'>\\%?\\{?({object}[^<>\\{\\}]+)"
      "(?i)'OperationType'>({operation}[^<]+)<"
      "(?i)'HandleId'>({handle_id}[^<]+)<"
      "(?i)'Properties'>[\\-\\\\r\\\\n\\s]*({properties}[^<]+?)[\\-\\\\r\\\\n\\s]*<"
    ]
    ParserVersion = "v1.0.0"
  

}
```