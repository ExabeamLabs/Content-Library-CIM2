#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-user-success-4648"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""EVENT_ID="4648""""
"""EVENT_TASK="Logon""""
"""A logon was attempted using explicit credentials"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)"""
"""({event_name}A logon was attempted using explicit credentials)"""
"""sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""EVENT_ID="{0,20}({event_code}\d+)"""
"""EVENT_HOST="({host}[^"]+)"""
"""EVENT_USERNAME="(-|({domain}[^\\]+)\\+(-|({user}[\w\.\-]{1,40}\$?)))"""
"""Logon ID:\s+({login_id}[^\s]+)\s+Logon GUID"""
"""Subject(:|=)[\s;]*Security ID(:|=)\s*(\\NULL SID|({user_sid}[^=:]*?))[\s;]*Account Name(:|=)"""
"""Subject(:|=)[^"]+?Account Name(:|=)\s*(?:-|SYSTEM|({user}[\w\.\-]{1,40}\$?))[\s;]*Account Domain(:|=)"""
"""Subject(:|=)[^"]+?Account Domain(:|=)\s*(?:-|NT Service|({domain}[^\s]*?))[\s;]*Logon ID(:|=)"""
"""Subject(:|=)[^"]+?Logon ID(:|=)\s*({login_id}[^=:]*?)[\s;]*Logon GUID(:|=)"""
"""Subject(:|=)[^"]+?Logon GUID(:|=)\s*\{({user_login_guid}[^}]+)\}[\s;]*Account Whose"""
"""Used(:|=);?\s*Account Name(:|=)\s*({dest_user}[^\s;@]+?)(@({dest_domain}[^\s;]+?))?[\s;]*Account Domain(:|=)"""
"""Used(:|=)[^"]+?Account Domain(:|=)\s*(|({dest_domain}[^=:]*?))[\s;]*Logon GUID(:|=)"""
"""Used(:|=)[^"]+?Logon GUID(:|=)\s*\{({account_login_guid}[^=:]*?)\}[\s;]*Target Server(:|=)"""
"""Target Server Name(:|=)\s*({dest_host}[\w\-.]*?)[\s;]*Additional Information(:|=)"""
"""Additional Information(:|=)\s*({dest_service_name}[^=:]*?)[\s;]*Process Information(:|=)"""
"""Process ID(:|=)\s*({process_id}[^=:]*?)[\s;]*Process Name(:|=)"""
"""Process Name(:|=)\s*(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?\s*({process_name}[^\\\/]+?)))\s+Network"""
"""Network Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
]
DupFields = [
"dest_user->account",
"dest_domain->account_domain"
]
ParserVersion = "v1.0.0"


}
```