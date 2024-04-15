#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-password-modify-4723"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """An attempt was made to change"""
]
Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s((?i)am|pm))"""
  """({event_name}An attempt was made to change an account's password)"""
  """"agent_hostname":"({host}[^"]+)""""
  """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\+\d\d\d\d)"""
  """\Wrt=({time}\d+)"""
  """Security,(rn=)?({event_id}[\d]+)"""
  """({host}[\w.\-]+)\s*:\s+An attempt was made to change"""
  """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)"""
  """({result}((Success|Failure|Audit)\s+\w+)|Information)(\s+|\s*,\s*|#011)({host}[\w\.\-]+)"""
  """"TimeGenerated":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
  """"(?i)Computer":"({host}[\w\-.]+)"""
  """EvntSLog:\s*\[({result}.+?)\]"""
  """;\s+Type = "({result}[^"]+)""""
  """Keywords=({result}.+?)\s+\w+="""
  """Event Type : ({result}.+?)\.\s+Log Type :"""
  """\Wact=({action}.+?)\s+(\w+=|$)"""
  """({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing"""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s)"""
  """Computer\s+:\s+({host}[\w\-]+)"""
  """({event_code}4723)"""
  """Subject.+?Security ID:\s+({user_sid}[^:]+?)(\\[nrt]\s+|\s+)Account Name"""
  """Subject.+?Account Name:\s+({user}[^:]+?)(\\[nrt]\s+|\s+)Account Domain"""
  """Account Domain:\s+({domain}[^:]+?)(\\[nrt]\s+|\s+)Logon ID:\s+({login_id}\w+)"""
  """Target Account.+?Security ID:\s+({dest_user_sid}[^:]+?)(\\[nrt]\s+|\s+)Account Name:"""
  """Target Account.+?Account Name:\s*({dest_user}[^:\s]+?)\s+Account Domain:\s*({dest_domain}[^:]+?)\s+Additional"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsntdom=({domain}.+?)(\\[nrt]\s+|\s+)(\w+=|$)"""
  """\Wshost=({src_host}.+?)\s+(\w+=|$)"""
  """\Wduser=(({domain}[^\\=]+)\\+)?({dest_user}[^\s\\=]+)"""
  """\Wsuser=(({domain}[^\\=]+)\\+)?({user}[^\s\\=]+)"""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[^\\\s"]+)"""
  """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"TargetSid":"({dest_user_sid}[^\s"]+)"""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^\\]+))\\?""""
  """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?""""
  """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?""""
  """TargetDomainName\\?"+:\\?"+({dest_domain}[^\s"\\]+)\\?""""
  """"TargetSid\\?"+:\\?"+({dest_user_sid}[^"\\]+)"""
  """TargetUserName\\?"+:\\?"+({dest_user}[^\\]+)\\?""""
  """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[^\\]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```