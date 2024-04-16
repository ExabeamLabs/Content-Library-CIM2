#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-47-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyyMMddHHmmss.SSS"
Conditions = [
"""EventCode = 47"""
""""A member was added to a security-enabled """
"""TimeGenerated = """
]
Fields = [
"""({event_name}A member was added to a security-enabled [\w\s]+ group)"""
"""Computer(Name)? = "+({host}[^"]+)""""
"""EventCode = ({event_code}\d+)"""
"""TimeGenerated = "({time}[\d]+.\d\d\d)"""
"""A member was added to a security-enabled ({group_type}[^\s]+) group"""
"""Subject:.+?Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:\s+({domain}[^\s]+)\s+Logon ID:\s+({login_id}[^\s]+)\s+"""
"""Member:\s+Security ID:\s+({account_id}(?=[^\\]+\\)({sid_domain}[^\\]+)\\({dest_user_sid}.+?)|(?:.+?))\s+Account Name:"""
"""Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s+Group:"""
"""Group:\s+Security ID:\s+({group_id}[^\s]+)\s+Group Name:"""
"""Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:"""
"""Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)\s+Additional"""
"""Group:\s+(\\r\s\\t)?Security ID:\s*(\\t)?({group_id}[^\s]+)\s*(\\r\s\\t)?Group Name:"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```