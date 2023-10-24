#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-computer"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [
    """Security ID:"""
    """Logon ID:"""
    """A member was removed from a security-enabled"""
    """Computer"""
  ]
  Fields = [
      """({event_name}A member was removed from a security-enabled [\w\s]+ group)""",
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """"agent_hostname":"({host}[\w\-.]+)"""",
      """"computer":"({host}[\w\-.]+)"""",
      """Computer_name:({host}[\w\-\.]+)"""
      """(?i)(success|audit)\s+\w+\s+({host}[\w\-.]+)""",
      """"?Event(ID>)?(Code["\s]*(:|=|\\=)\s*"?)?({event_code}\d+)""",
      """({event_code}\d+)\s+Microsoft-Windows-Security-Auditing""",
      """A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group""",
      """Account Name\s*:\s*(\\t|\\n|\\r)*({user}[\w\.\-]{1,40}\$?)\s*(\\t|\\n|\\r)*\s*Account Domain\s*:\s*(\\t|\\n|\\r)*({domain}[^\\\s]+)\s*(\\t|\\n|\\r)*""",
      """Logon ID:\s*(\\t|\\n|\\r)*({login_id}[^\\\s]+)(\\t|\\n|\\r)*\s*""",
      """Member:\s*(\\t|\\n|\\r)*Security ID\s*:\s*(\\t|\\n|\\r)*({dest_user_sid}[^:]+?)\s*(\\t|\\n|\\r)*Account Name:""",
      """Member:.+?Security ID\s*:\s*(\\t|\\n|\\r)*({dest_user_sid}[^\\\s]+)"""
      """Account Name\s*:\s*(\\t|\\n|\\r)*(.+?({user_dn}CN\\*=.+?,({user_ou}OU.+?DC\\*=[\w-]+)))\s*(\\t|\\n|\\r)*Group:""",
      """Group\s*:.+?Security ID\s*:\s*(\\t|\\n|\\r)*({group_id}[^\\\s]+)\s*""",
      """Group:.+?(Group|Account) Name\s*:\s*(\\t|\\n|\\r)*({group_name}.+?)?(\\t|\\n|\\r)*\s*(\\t|\\n|\\r)*(Group|Account) Domain\s*:\s*(\\t|\\n|\\r)*({group_domain}[^\\\s]+)\s*""",
      """"EventID":({event_code}\d+)""",
      """"ComputerName":"({host}[\w\-.]+)""""
      """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```