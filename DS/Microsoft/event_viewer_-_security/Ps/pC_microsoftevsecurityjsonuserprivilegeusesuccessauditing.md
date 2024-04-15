#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-auditing"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""An operation was attempted on a privileged object"""
"""/Microsoft-Windows-Security-Auditing"""
]
Fields = [
"""({event_name}An operation was attempted on a privileged object)"""
"""\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4674\)"""
"""Event Type\s*:\s*({result}.+?)\.\s+Log Type"""
"""Type\s*=\s*\"({result}[^\";]+)\""""
"""Keywords=({result}.+?);?\s*Message="""
"""\s*Source Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Source Port(:|=)"""
"""({event_code}4674)"""
"""Process Name(:|=)\s*(?: |({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))[\s;]*Requested"""
"""\s*Account Name(:|=)\s*(?:-|({user}.+?))[\s;]*Account Domain(:|=)\s*({domain}.+?)[\s;]*Logon ID(:|=)\s*({login_id}.+?)[\s;]*Object(:|=)"""
"""\s*Object Server(:|=)\s*({object_server}.+?)[\s;]*Object Type(:|=)\s*(?:-|({object_type}.+?))[\s;]*Object Name(:|=)\s*(?:|-|({object}.+?))[\s;]*Object Handle"""
"""Desired Access(:|=)\s*({access}.+?)[\s;]*Privileges(:|=)\s*({privileges}.+?)(\s+\d+|\"|,|;|\s+User:|\s$)"""
"""\"Account\":\"((NT AUTHORITY|({domain}[^\\\s\"]+))\\+)?(LOCAL SERVICE|({user}[^\\\s\"]+))\s*\""""
"""\"TargetAccount\":\"(({dest_domain}[^\\\s\"]+)\\+)?({dest_user}[^\\\s\"]+)"""
"""\"SubjectUserSid\":\"({user_sid}[^\s\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\s\"]+)"""
"""\"ObjectServer\":\"(-|({object_server}[^\s\"]+))"""
"""\"ObjectName\":\"(-|({object}[^\s\"]+))"""
"""\"ObjectType\":\"(-|({object_type}[^\s\"]+))"""
"""\"ProcessName\":\"(?: |({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))\s*\""""
]
DupFields = [
"host->dest_host"
"directory->process_dir"
]
ParserVersion = "v1.0.0"


}
```