#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-computer"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
    """Security ID:"""
    """Logon ID:"""
    """A member was removed from a security-enabled"""
    """Computer"""
  ]
  Fields = [
      """({event_name}A member was removed from a security-enabled [\w\s]+ group)""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """"agent_hostname":"({host}[\w\-.]+)"""",
      """"computer":"({host}[\w\-.]+)"""",
      """(?i)Computer_name(\\*")?:(\\*")?({host}[\w\-\.]+)"""
      """(?i)(((audit|success)( |_)(success|audit))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*"""
      """({event_code}\d+)\|\s+devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
      """"?Event(ID>)?(Code["\s]*(:|=|\\=)\s*"?)?({event_code}\d+)""",
      """({event_code}\d+)\s+Microsoft-Windows-Security-Auditing""",
      """A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group""",
      """Account Name\s*:((\\)*[rnt])*\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*((\\)*[rnt])*Account Domain\s*:((\\)*[rnt])*\s*({domain}[^\s\\:]+)"""
      """Logon ID:\s*({login_id}[^\s]+)\s+"""
      """Group:.+?(Group|Account) Name\s*:(\\*(r|n|t|\s))*({group_name}.+?)?(\\*(r|n|t|\s))*(Group|Account) Domain\s*:(\\*(r|n|t))*({group_domain}.+?)?(\\*(r|n|t|\s))*Additional Information:"""
      """Account Name\s*:\s*(\\t|\\n|\\r)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\t|\\n|\\r)*\s*Account Domain\s*:\s*(\\t|\\n|\\r)*({domain}[^\\\s]+)\s*(\\t|\\n|\\r)*""",
      """Logon ID:\s*(\\t|\\n|\\r)*({login_id}[^\\\s]+)(\\t|\\n|\\r)*\s*""",
      """"+SubjectUserSid\\?"+:\\?"+({user_sid}[^"\\<,]+)"""
      """Member:\s*(\\t|\\n|\\r)*Security ID\s*:\s*(\\t|\\n|\\r)*(({dest_user_sid}S-[^:]+?)|({account_domain}[^\\\s:]+)\\+({account_name}[^:]+?))\s*(\\t|\\n|\\r)*Account Name:""",
      """Member:.+?Security ID\s*:\s*(\\t|\\n|\\r)*({dest_user_sid}S-\d+-[^\\\s]+)"""
      """Account Name\s*:\s*(\\*(r|n|t))*(.+?({user_dn}CN\\*=.+?,({user_ou}OU.+?DC\\*=[\w-]+)))\s*(\\*(r|n|t))*Group:""",
      """Group\s*:(\\*(r|n|t))*.+?Security ID\s*:\s*(\\*(r|n|t))*({group_id}[^\\\s]+)\s*""",
      """Group:.+?(Group|Account) Name\s*:\s*(\\t|\\n|\\r)*({group_name}.+?)?(\\t|\\n|\\r)*\s*(\\t|\\n|\\r)*(Group|Account) Domain\s*:\s*(\\t|\\n|\\r)*({group_domain}[^\\\s]+)\s*""",
      """"EventID":({event_code}\d+)""",
      """"ComputerName":"({host}[\w\-.]+)""""
      """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
      """thread"+:[^@]+?"+id"+:({thread_id}\d+)"""
      """"record_id"+:({event_id}\d+)"""
      """"task"+:"+({task_name}[^"]+)"""
      """"event_id\\?"+:({event_code}\d+)"""
      """"(?:winlog\.)?computer_name"+:"+({host}[^"]+)"""
      """"(?i)Hostname\\*"+:\\*"+({host}[\w\-.]+)"""
      """"keywords"+:\["+({result}[^"]+)"""
      """"pid"+:({process_id}\d+)"""
      """"os":[^@]+?"name":"({os}[^"]+)"""
      """"+activity_id"+:"+\{({activity_id}[^}]+)"""
      """"action"+:"+({action}[^"]+)"""
      """"+MemberSid\\?"+:\\?"+({account_id}[^"\\]+)"""
      """ComputerName =({host}[\w\-.]+)"""
  ]
  DupFields = [
    "host->src_host"
    "user_dn->member"
  ]
  ParserVersion = "v1.0.0"


}
```