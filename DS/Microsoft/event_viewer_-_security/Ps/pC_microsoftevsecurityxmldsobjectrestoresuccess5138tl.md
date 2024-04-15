#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-restore-success-5138-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5138<"
      "a directory service object was undeleted."
    ]
    Fields = [
      "(?i)({event_name}A directory service object was undeleted)"
      "(?i)({event_code}5138)"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?|({dest_host}[^<]+))<"
      "(?i)Security ID:\\s+({user_sid}[^\\s]+?)\\s+Account Name:\\s+({user}[^\\s]+?)\\s+Account Domain:\\s+((?i)(NA)|({domain}[^\\s]+?))\\s+Logon ID:\\s+({login_id}[^\\s]+)"
      "(?i)Class:\\s+({object_class}[^:]+?)\\s+Operation:"
      "(?i)Object:[^\\{\\}]+?New DN:\\s+({object_dn}[^\\s]+)"
      "(?i)Object:\\s+Old DN:[^\\{\\}]+?({object_ou}OU[^\\s]+?)\\s+GUID:"
      "(?i)Directory Service:\\s*Name:\\s*({service_name}[^\\s]+)\\s+Type:\\s*({service_type}[^:]*?Services)"
      "(?i)<Data Name ='ObjectGUID'>\\{({guid}[^<\\}]+)\\}<"
      "(?i)<Data Name ='OpCorrelationID'>\\{({correlation_id}[^\\}<]+)\\}<"
    ]
    ParserVersion = "v1.0.0"
  

}
```