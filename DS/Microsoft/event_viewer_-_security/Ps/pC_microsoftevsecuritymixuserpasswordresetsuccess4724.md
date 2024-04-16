#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-password-reset-success-4724"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy"]
Conditions = [
  """An attempt was made to reset an account's password"""
]
Fields = [
  """"agent_hostname":"({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))""""
  """"computer":"({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))""""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
  """TimeGenerated=({time}\d{10})""",
  """(TimeGenerated|EventTime)":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({host}[\w\-.]+)\s"""
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|10\.\.0\.01|({dest_host}[\w\-.]+))\s"""
  """({event_name}An attempt was made to reset an account's password)"""
  """Security,?\s*(rn=)?({event_id}[\d]+)"""
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
  """(?i)(((audit|success)( |_)(success|audit))|information)(,|\s+)(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))"""
  """(::ffff:)?((?i)KAFKA_CONNECT_SYSLOG|({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+))))\s*:\s+An attempt was made to reset an account's password"""
  """({event_code}4724)"""
  """(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\/Microsoft-Windows-Security-Auditing"""
  """Computer(\w+)?["\s]*(:|=)\s*"?(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+?)))("|\s)"""
  """Computer : (::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))"""
  """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(10\.\.0\.01|am|pm|\d{4}|({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))))\s+(\w+=)?"""
  """Subject:[^=]+?Security ID:\s+(NT AUTHORITY\\SYSTEM|({user_sid}[^:]+?))\s+Account Name:"""
  """\s*Source Address:\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Source Port:"""
  """Subject:[^=]+?Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:\s+((?i)NT AUTHORITY|({domain}[^:]+?))\s+Logon ID"""
  """Logon ID:(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*"""
  """Target Account[^=]+?Security ID:(\\t|\\r|\\n|\s)*(|({dest_user_sid}[^:]+?))(\\t|\\r|\\n|\s)+Account Name:(\\t|\\r|\\n|\s)*(|({dest_user}[\w\.\-]{1,40}\$?)|({dest_user_full_name}[^\s]+))(\\t|\\r|\\n|\s)+Account Domain:(\\t|\\r|\\n|\s)+({dest_domain}[^",\s]+)"""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\"]+)\\?""""
  """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)\\?""""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\\?""""
  """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\"]+)\\?""""
  """TargetDomainName\\?"+:\\?"({dest_domain}[^\s\\"]+)\\?""""
  """"TargetSid\\?"+:\\?"({dest_user_sid}[^\\"]+)"""
  """TargetUserName\\?"+:\\?"(({dest_user}[\w\.\-]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))\\?""""
  """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\"]+))\\?""""
  """"Hostname\\?":\\?"({host}[\w\-.]+)\\?""""
  """"source_ip"\s*:\s*"(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*""""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
]
ParserVersion = "v1.0.0"


}
```