#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-5145-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5145</eventid>"
      "a network share object was checked to see whether client can be granted desired access"
      "<data name='sharename'>"
    ]
    Fields = [
      "(?i)({event_code}5145)"
      "(?i)({event_name}A network share object was checked to see whether client can be granted desired access)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)ProcessID='({process_id}\\d+)'"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<Computer>(\\d{1,3}.\\d{1,3}.\\d{1,3}.\\d{1,3}|({dest_host}[^<]+)</Computer>)"
      "(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<]+)</Data>"
      "(?i)<Data Name ='SubjectUserName'>({user}[^\\s<]+)</Data>"
      "(?i)<Data Name ='SubjectDomainName'>(|NT AUTHORITY|({domain}[^<]+))</Data>"
      "(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"
      "(?i)<Data Name ='ObjectType'>({file_type}[^<]+)</Data>"
      "(?i)<Data Name ='IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name ='IpPort'>({src_port}\\d+)"
      "(?i)<Data Name ='ShareName'>({share_name}[^<]+)</Data>"
      "(?i)<Data Name ='RelativeTargetName'>({f_parent}[^<]+?\\\\+)?(?:|({file_name}[^\\\\:<]*?(\\.\\s*({file_ext}[^\\W_\\\\.]+?))?))?\\?</Data>"
      "(?i)<Data Name ='AccessList'>\\s*({access}[^<]+)\\s*</Data>"
      "(?i)Accesses:[^:]*?({access}SYNCHRONIZE|Execute|Traverse|Read|READ|WRITE_DAC|WRITE_OWNER|WriteAttributes|WriteEA|WriteData|AppendData|delete|Delete)[^:]*?Access Check Results:"
      "(?i)<Data Name ='ShareLocalPath'>(?:[\\\\\\?]+)?(?:\\s*|({share_path}(({d_parent}[^<>]+)\\\\)?({d_name}\\s*\\S[^\\\\<>]+?)?)\\\\?)<\\/Data>"
      "(?i)<Data Name ='AccessReason'>\\s*(-|({access_reason}[^<]+?))\\s*</Data>"
      "(?i)<Keywords><Keyword>({result}[^<]+)</Keyword>"
    ]
  

}
```