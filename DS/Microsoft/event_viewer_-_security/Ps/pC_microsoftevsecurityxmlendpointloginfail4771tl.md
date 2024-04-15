#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-fail-4771-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4771</eventid>"
      "<data name='targetsid'>"
    ]
    Fields = [
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)<Data Name ='TargetSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"
      "(?i)<Data Name ='Status'>({result_code}[^<]+)</Data>"
      "(?i)<Data Name ='TargetUserName'>(?=\\w)({user}[^<]+)</Data>"
      "(?i)<Data Name ='ServiceName'>\\w+\\/(?=\\w)({domain}[^<]+)</Data>"
      "(?i)<Data Name ='IpAddress'>(::[\\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?</Data>"
      "(?i)({event_name}Kerberos pre-authentication failed)"
    ]
    DupFields = [
      "result_code->failure_code"
    ]
    ParserVersion = "v1.0.0"
  

}
```