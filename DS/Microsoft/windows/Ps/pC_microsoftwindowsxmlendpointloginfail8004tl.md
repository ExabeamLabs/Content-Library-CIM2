#### Parser Content
```Java
{
Name = "microsoft-windows-xml-endpoint-login-fail-8004-tl"
    Vendor = "Microsoft"
    Product = "Windows"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>8004</eventid>"
      "security policy network security:"
      "restrict ntlm:"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<>]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventRecordID>({event_id}[^<>]+)<"
      "(?i)Name ='DomainName'>(NULL|({domain}[^<>]+))<"
      "(?i)<EventID>({event_code}[^<>]+)</EventID>"
      "(?i)({event_name}Domain Controller Blocked Audit: Audit NTLM authentication to this domain controller)"
      "(?i)<Execution ProcessID='({process_id}\\d+)'"
      "(?i)Name ='SChannelName'>({resource}[^<>]+)<"
      "(?i)Name ='WorkstationName'>\\\\*(NULL|({src_host}[^<>]+))<"
      "(?i)Name ='UserName'>(({email_address}[^@\\s<>]+@[^@\\s<>]+)|({user}[^<>]+?))\\s*<"
      "(?i)<Security UserID='({user_sid}[^<>\\/']+)"
      "(?i)security policy Network Security:\\s*Restrict NTLM:\\s*({policy_name}[^\\.:]+)"
    ]
    DupFields = [
      "resource->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```