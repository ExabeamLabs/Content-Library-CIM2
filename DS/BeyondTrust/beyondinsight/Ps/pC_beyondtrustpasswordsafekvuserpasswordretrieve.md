#### Parser Content
```Java
{
Name = "beyondtrust-passwordsafe-kv-user-passwordretrieve"
Vendor = "BeyondTrust"
Product = "BeyondInsight"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""Event Desc: Password Retrieve"""
"""Agent ID: PBPS"""
"""Failed: False"""
]
Fields = [
"""LogTime:\s*({time}\d+\/\d+\/\d+ \d+:\d+:\d+)"""
"""User:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+\s)?\w+:"""
"""Source Host:\s*({host}[^\s]+)"""
"""Event Subject:\s*0*({src_ip_1}\d+\.)0*({src_ip_2}\d+\.)0*({src_ip_3}\d+\.)0*({src_ip_4}\d+)"""
"""Target:.*?Asset:({dest_host}[^\s]+)\s+\w+:"""
"""Target:.*?MAccount:({dest_user}[^\s]+)\s+\w+:"""
"""RoleUsed:\s*({privileges}.+?)\s+\w+:"""
"""Agent ID:\s*({event_code}PBPS)"""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```