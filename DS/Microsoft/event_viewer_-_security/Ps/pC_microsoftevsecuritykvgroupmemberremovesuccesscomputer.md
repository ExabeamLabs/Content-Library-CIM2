#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-computer"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [
    """Security ID:"""
    """Logon ID:"""
    """A member was removed from a security-enabled"""
    """Computer"""
  ]
  Fields = [
      """({event_name}A member was removed from a security-enabled [\w\s]+ group)""",
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """"agent_hostname":"({host}[^"]+)"""",
      """"computer":"({host}[^"]+)"""",
      """Computer_name:({host}[\w\-\.]+)"""
      """(?i)(success|audit)\s+\w+\s+({host}[\w\-.]+)""",
      """"?Event(ID>)?(Code["\s]*(:|=|\\=)\s*"?)?({event_code}\d+)""",
      """({event_code}\d+)\s+Microsoft-Windows-Security-Auditing""",
      """A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group""",
      """Account Name\s*:\s*({user}[^\\\s]+)[\s\\n]*Account Domain\s*:\s*({domain}[^\\\s]+)[\s\\n]+""",
      """Logon ID:\s*({login_id}[^\\\s]+)[\\n\s]*""",
      """Member:\s*Security ID\s*:\s*({user_sid}(?=[^\\]+\\)({sid_domain}[^\\]+)\\({account_id}[^\\\s]+)|(?:.*?))\s*Account Name:""",
      """Member:\s*.+?Security ID\s*:\s*({user_sid}[^\\\s]+)"""
      """Account Name\s*:\s*(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s*Group:""",
      """Group\s*:.+?Security ID\s*:\s*({group_id}[^\\\s]+)\s*""",
      """Group:.+?(Group|Account) Name\s*:\s*({group_name}.+?)?[\s\\n]*(Group|Account) Domain\s*:\s*({group_domain}[^\\\s]+)\s*""",
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```