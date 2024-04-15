#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-add-success-47-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      ">47"
      ">a member was added to a security-enabled"
    ]
    Fields = [
      "(?i)({event_name}A member was added to a security-enabled [\\w\\s]+ group)"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<EventID>({event_code}[^<]+)</EventID>"
      "(?i)(Success Audit|Audit Success|Information)<\\d+>({host}[^<]+)<"
      "(?i)>({event_code}\\d+)<\\d+>Microsoft-Windows-Security-Auditing"
      "(?i)A member was added to a security-enabled ({group_type}[^\\s]+) group"
      "(?i)Subject:.+?Account Name:\\s*(#011)*({user}[^\\s#]+)\\s*(#011)*\\s*Account Domain"
      "(?i)<Data Name ='SubjectUserName'>(\\#011)*({user}[^\\s#]+?)\\s*(\\#\\d+)*\\s*<"
      "(?i)Subject:.+?Account Domain:\\s*(\\#011)*({domain}[^\\s#]+?)\\s*(\\#011)*\\s*Logon ID"
      "(?i)Logon ID:\\s*(\\#011)*({login_id}[^\\s#]+?)\\s*(\\#011)*\\s*Member:"
      "(?i)Member:.*?Security ID:\\s*({account_id}(?=[^\\\\:]+\\\\)({sid_domain}[^\\\\:]+)\\\\({user_sid}[^\\s]+)|(?:[^\\s]+))\\s*Account Name:"
      "(?i)Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\\w-]+))|(?:.+?))\\s*Group:"
      "(?i)Group:\\s*Security ID:\\s*({group_id}.+?)\\s*(Group|Account) Name"
      "(?i)Group:.+?(Group|Account) Name:\\s*(\\#011)*({group_name}.+?)\\s*(\\#011)*\\s*(Group|Account) Domain:"
      "(?i)Group:.+?(Group|Account) Domain:\\s*(\\#011)*({group_domain}[^\\s#]+)\\s*(\\#011)*\\s*(Additional Information:)?"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```