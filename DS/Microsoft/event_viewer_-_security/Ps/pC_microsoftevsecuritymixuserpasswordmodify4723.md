#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-password-modify-4723"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "MM/dd/yyyy HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
Conditions = [
  """An attempt was made to change"""
]
Fields = [
  """({event_name}An attempt was made to change an account's password)"""
  """"agent_hostname":"({host}[\w\-.]+)""""
  """Security,(rn=)?({event_id}[\d]+)"""
  """({host}[\w.\-]+)\s*:\s+An attempt was made to change"""
  """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)"""
  """({result}((Success|Failure|Audit)\s+\w+)|Information)(\s+|\s*,\s*|#011)({host}[\w\.\-]+)"""
  """TimeGenerated=({time}\d{10})""",
  """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun)\s+({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
  """"(?i)Computer":"({host}[\w\-.]+)"""
  """EvntSLog:\s*\[({result}.+?)\]"""
  """;\s+Type = "({result}[^"]+)""""
  """Keywords=({result}.+?)\s+\w+="""
  """Event Type : ({result}.+?)\.\s+Log Type :"""
  """\Wact=({result}.+?)\s+(\w+=|$)"""
  """({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing"""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}[\w\-.]+?)("|\s)"""
  """Computer\s+:\s*({host}[\w\-.]+)"""
  """({event_code}4723)"""
  """Subject.+?Security ID:\s*(\\r|\\n|\\t)*({user_sid}S-[^:\s]+?)(\\r|\\n|\\t)*\s*Account Name"""
  """Subject.+?Account Name:\s*(\\r|\\n|\\t)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\r|\\n|\\t)*\s*Account Domain"""
  """Account Domain:\s*({domain}[^:]+?)(\\[nrt]\s+|\s+)Logon ID:\s*({login_id}\w+)"""
  """Target Account.+?Security ID:\s*(\\r|\\n|\\t)*({dest_user_sid}S-[^:\s]+?)(\\n|\\r|\\t)*\s*Account Name:"""
  """Target Account.+?Account Name:(\\t|\\r|\\n|\s)*({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*({dest_domain}[^:]+?)(\\t|\\r|\\n|\s)*Additional"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsntdom=({domain}.+?)(\\[nrt]\s+|\s+)(\w+=|$)"""
  """\Wshost=({src_host}.+?)\s+(\w+=|$)"""
  """\Wduser=(({domain}[^\\=]+)\\+)?({dest_user}[^\s\\=]+)"""
  """\Wsuser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}S-[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """""TargetSid":"({dest_user_sid}S-[^\s"]+)""""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\"]+)\\?""""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
  """SubjectUserSid\\?"+:\\?"+({user_sid}S-[^\\"]+)\\?""""
  """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^\\"]+))\\?""""
  """TargetDomainName\\?"+:\\?"+({dest_domain}[^\s"\\]+)\\?""""
  """"TargetSid\\?"+:\\?"+({dest_user_sid}S-[^"\\]+)""""
  """TargetUserName\\?"+:\\?"+({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?""""
  """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d)\s+(?i)(AM|PM)"""
]
DupFields = ["src_user->user", "src_domain->domain"]
ParserVersion = "v1.0.0"


}
```