#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4769-12"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""ComputerName ="""
"""EventID=4769"""
"""Microsoft-Windows-Security-Auditing"""
]
Fields = [
"""({event_name}A Kerberos service ticket was requested)"""
"""DetectTime(?::|=)({time}\d+-\d+-\d+ \d+:\d+:\d+)"""
""""dhn":"({host}[^-"]+)"""
"""({event_code}4769)"""
"""Account Domain(?::|=)({domain}[^\s]+)"""
"""Account Name(?::|=)(?:[^\/]+\/)?({user_upn}[^@]+@[^\s]+)"""
"""Failure Code(?::|=)({result_code}[^\s]+)"""
"""Ticket Encryption Type(?::|=)({ticket_encryption_type}[^\s]+)"""
"""Client Address(?::|=)\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""ComputerName(?::|=)({host}[^\s]+)\s"""
"""Client Port(?::|=)({src_port}\d+)"""
"""Logon GUID(?::|=)\{?({user_login_guid}[^\}\s]+)"""
"""Ticket Options(:|=)\s*({ticket_options}[^\s]+)"""
"""EventType(:|=)\s*({result}[^\s]+)"""
"""Account Name(:|=)\s*([^\/]+\/)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?[\s;]*Account"""
]
ParserVersion = "v1.0.0"


}
```