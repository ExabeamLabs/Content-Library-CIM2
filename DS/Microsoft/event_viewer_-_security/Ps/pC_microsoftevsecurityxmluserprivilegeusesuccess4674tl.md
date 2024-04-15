#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-use-success-4674-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4674</eventid>"
      "<data name='subjectusername'>"
      "<message>an operation was attempted on a privileged object"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d\\d\\d\\d\\d\\d\\dZ)"
      "(?i)<Keywords>({result}[^<]+)<"
      "(?i)<Computer>({host}[\\w.\\-]+)<"
      "(?i)({event_code}4674)"
      "(?i)<Data Name ='SubjectUserSid'>\\s*(({domain}[^\\\\<]+)\\\\)?({user}[^<]+)<"
      "(?i)<Data Name ='SubjectUserName'>({user}[^<]+?)<"
      "(?i)<Data Name ='SubjectDomainName'>({domain}[^<]+?)<"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+?)<"
      "(?i)<Data Name ='ObjectServer'>(-|({object_server}[^<]+?))<"
      "(?i)<Data Name ='PrivilegeList'>({privileges}[^<]+?)<"
      "(?i)<Data Name ='ProcessName'>({process_path}({process_dir}[^<]*?)({process_name}[^\\\\<]+?))<"
      "(?i)({event_name}An operation was attempted on a privileged object)"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```