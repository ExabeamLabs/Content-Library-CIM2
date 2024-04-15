#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-activity-success-4662-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4662<"
    ]
    Fields = [
      "(?i)({event_name}An operation was performed on an object)"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserSid'>({user_sid}[^<]+)"
      "(?i)<Data Name(\\\\)?='SubjectUserName'>(-|CN=[^<]+|({user}[^<]+))"
      "(?i)<Data Name(\\\\)?='SubjectDomainName'>(-|({domain}[^<]+))"
      "(?i)<Data Name(\\\\)?='SubjectLogonId'>({login_id}[^<]+)"
      "(?i)<Data Name(\\\\)?='ObjectServer'>({ds_object_class}[^<]+)"
      "(?i)<Data Name(\\\\)?='ObjectType'>({object_type}[^<]+)"
      "(?i)<Data Name(\\\\)?='ObjectName'>({object}[^<]+)"
      "(?i)<Data Name(\\\\)?='OperationType'>({operation}[^<]+)"
      "(?i)<Data Name(\\\\)?='Properties'>\\s*(-|({properties}[^<]+?))\\s*<"
      "(?i)<Keyword>({result}[^<]+)<"
      "(?i)Accesses:\\s*({access}[^:]+?)\\s+Access Mask:"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```