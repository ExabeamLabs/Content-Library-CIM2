#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-memberwasadded"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = ["""A member was added to a security-enabled""","""Subject:""","""Security ID:"""]
  Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
      """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
      """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """({time}\w+ \d+ \d+:\d+:\d+ \d{4})\s+47\d\d\s+Microsoft""",
      """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
      """\s(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}[\w.\-]+)\s""",
      """ComputerName\\=({host}[\w\-.]+)""",
      """Computer_name:({host}[\w\-\.]+)"""
      """Computer(\w+)?["\s]+(:|=)\s*"?({host}.+?)("|\s|;)""",
      """({event_code}4728|4732|4756)""",
      """({event_code}47\d\d)(\s+|,)Microsoft-Windows-Security-Auditing""",
      """"EventID":"({event_code}\d+)""",
      """EventCode\\=({event_code}\d+)""",
      """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s\\n]*Account Domain:\s*({domain}[^\s]+?)[\s\\n]*Logon ID:""",
      """Logon ID:\s*({login_id}[^\s\\]+)""",
      """Member:\s*Security ID:\s*(({dest_user_sid}S-\d+-[^\s]+)|({account_domain}[^\\\s]+)\\+({account_name}.+?)|(?:.+?))\s*Account Name:""",
      """A member was added to a security-enabled ({group_type}\w+) group""",
      """Account Name:\s*(?:-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+)))?\s*Group:""",
      """Group:\s*Security ID:\s*(None|({group_id}[^\s]+))\s*(Group|Account) Name:\s*(None|({group_name}.+?))?\s*(Group|Account) Domain:\s*(None|({group_domain}[^\s]+))""",
      """Subject:\s+[^:]+:\s*({user_sid}.+?)\s+Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
      """Security(,|\s+)({event_id}\d+)""",
      """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """"MemberName":"(?:-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+)))?""",
      """"TargetAccount":"(({group_domain}[^\\\s"]+)\\+)?({group_name}[^\\\s"]+)""",
      """"MemberSid":"({account_id}[^\s"]+)""",
      """"ManagementGroupName":"({group_name}[^\s"]+)""",
      """"SubjectLogonId":"({login_id}[^\s"]+)""",
      """"TargetSid":"({group_id}[^\s"]+)""",
      """"data\.system_name":"({host}[^"]+)"""",
      """"data\.id":"({event_code}\d+)"""",
      """EventType="*({result}[^"\s]+)""",
      """<Data Name ="MemberName(">|":")CN\\?=({member}[^>]+)<\/Data>"""
  ]
  DupFields = [
    "host->dest_host"
    "user->account" 
  ]
  ParserVersion = "v1.0.0"


}
```