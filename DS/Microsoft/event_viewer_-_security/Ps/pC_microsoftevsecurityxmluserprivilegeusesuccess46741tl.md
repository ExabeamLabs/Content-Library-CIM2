#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-use-success-4674-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<data name"
      "<eventid>4674</eventid>"
      "<event xmlns"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime[\\\\\\/]*='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Keywords>({result}.+?)</Keywords>"
      "(?i)<Computer>({host}[\\w.\\-]+)</Computer>"
      "(?i)({event_code}4674)"
      "(?i)<Data Name[\\\\\\/]*='SubjectUserSid'>\\s*(({domain}[^\\\\]+)\\\\)?({user}[^<]+)</Data>"
      "(?i)<Data Name[\\\\\\/]*='SubjectUserName'>({user}[^<]+?)</Data>"
      "(?i)<Data Name[\\\\\\/]*='SubjectDomainName'>({domain}[^<]+?)</Data>"
      "(?i)<Data Name[\\\\\\/]*='SubjectLogonId'>({login_id}[^<]+?)</Data>"
      "(?i)<Data Name[\\\\\\/]*='ObjectServer'>(-|({object_server}[^<]+?))</Data>"
      "(?i)<Data Name[\\\\\\/]*='PrivilegeList'>({privileges}[^<]+?)</Data>"
      "(?i)<Data Name[\\\\\\/]*='ProcessName'>({process_path}({process_dir}[^<]*?)({process_name}[^\\\\<]+?))</Data>"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```