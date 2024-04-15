#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-remove-success-memberremoved-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [
      "security id:"
      "logon id:"
      "a member was removed from a security-enabled"
      "computer"
      "<eventid>4733</eventid>"
    ]
    Fields = [
      "(?i)({event_name}A member was removed from a security-enabled [\\w\\s]+ group)"
      "(?i)({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \\d{1,2} \\d{1,2}:\\d{1,2}:\\d{1,2} 20\\d{2})"
      "(?i)Computer(Name|_name)?[\"\\s]*(:|=|\\\\=)\\s*\"?({host}.+?)(\"|\\s)"
      "(?i)\"?Event(ID)?Code[\"\\s]*(:|=|\\\\=)\\s*\"?({event_code}\\d+)"
      "(?i)({event_code}\\d+)\\s+Microsoft-Windows-Security-Auditing"
      "(?i)A member was removed from a security-enabled\\s*({group_type}[^\\s]+)\\s+group"
      "(?i)Account Name\\s*:\\s*({user}[^\\s]+)\\s*Account Domain\\s*:\\s*({domain}[^\\s]+)\\s+"
      "(?i)Logon ID:\\s*({login_id}[^\\s]+)\\s+"
      "(?i)Member:\\s*Security ID\\s*:\\s*({account_id}(?=[^\\\\]+\\\\)({sid_domain}[^\\\\]+)\\\\({user_sid}[^\\\\\\s]+)|(?:.*?))\\s*Account Name:"
      "(?i)Account Name\\s*:\\s*(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\\w-]+))|(?:.+?))\\s*Group:"
      "(?i)Group\\s*:\\s*Security ID\\s*:\\s*({group_id}[^\\s]+)\\s*"
      "(?i)Group:.+?(Group|Account) Name\\s*:\\s*({group_name}.+?)?\\s*(Group|Account) Domain\\s*:\\s*({group_domain}[^\\s]+)\\s*"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```