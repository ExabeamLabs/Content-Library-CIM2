#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""Account That Was Locked Out"""
]
Fields = [
"""hostname=({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+)),\s*\w+="""
""""agent_hostname":"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""""
"""computer":"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""""
"""<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({host}[\w\-.]+)\s"""
"""<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))\s"""
"""({event_name}A user account was locked out)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""({event_code}4740)"""
"""(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""
"""({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""
"""(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\/Microsoft-Windows-Security-Auditing \(4740\)"""
""""dhn":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^-"]+))"""
"""Computer : (::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""
"""Computer(\w+)?["\s]*(:|=)\s*"?(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))("|\s)"""
""""system_name":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""""
"""Security,?(\srn=|\s+)?({event_id}\d+)"""
"""Subject:.+?Account Name:(\\t|\\r|\\n|\s)*({src_user}[^:]+?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*(?=\w)({src_domain}[^:]+?)(\\t|\\r|\\n|\s)*Logon ID:(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*"""
"""Locked Out:\s+Security ID:\s*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+))\}?\s+Account Name:\s*(?=\w)({user}[\w\.\-]{1,40}\$?)\s+Additional""",
"""Account Name:(\\t|\\r|\\n|\s)*({dest_user}[\w\.\-]{1,40}\$?)"""
""""targetUserName":"({dest_user}[^"]+)"""",
"""Caller Computer Name:\s*([\\\/]+)?(::ffff:)?({src_host}[^\#\s\",<]+)"""
"""\Weventrecordid="({event_id}\d+)""""
"""Subject(:|=).+?Logon ID(:|=)(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*Account""",
"""Subject(:|=).+?Account Name(:|=)\s*({src_user}[^\s]*?)(\\n)*[\s;]*Account Domain(:|=)""",
"""Locked Out:(\\n)*\s+Security ID:\s*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+))\}?(\\n)*\s+Account Name:\s*(?=\w)({user}[\w\.\-]{1,40}\$?)(\\n)*\s*Additional""",
"""\W__li_source_path="({host}[\w\.-]+)"""",
]
DupFields = [
"host->dest_host"
"src_domain->domain"
]
ParserVersion = "v1.0.0"


}
```