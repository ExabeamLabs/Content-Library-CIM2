#### Parser Content
```Java
{
Name = "cyberark-pam-kv-app-activity-eventmessage"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "MMM dd HH:mm:ss"
Conditions = [ """,EventMessage""" , """Cyber-Ark Vault""" , """,ActingUserName""" ]
Fields = [
  """({time}\w+\s+\d\d(\s+\d\d\d\d)?\s+\d\d:\d\d:\d\d)"""
  """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+ProductName"""
  """({app}Cyber-Ark Vault)"""
  """ProductAccount="(({domain}[^\s"]+)\\+)?({account}[^\s"]+)"""
  """Process="?(NULL|({process_name}[^"\s;,]+))"""
  """EventId="?({event_code}\d+)"""
  """Severity="?({severity}\d+)"""
  """EventMessage="?({operation}[^"=,]+)"""
  """ActingUserName ="?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """User="?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """ActionObject="?({object}[^"=,]+)"""
  """ApplicationType="?({app_type}[^";=,]+)"""
  """DstHost=\s*({dest_host}[\w\-.]+)"""
  """Protocol=({protocol}[^\s;]+)"""
  """SessionID=({session_id}[^=\s;]+)"""
  """SrcHost=\s*({host}[\w\-.]+)"""
]
DupFields = ["operation->access"]
ParserVersion = "v1.0.0"


}
```