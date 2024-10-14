#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-47"
Vendor = "Microsoft"
Product = Event Viewer - Security
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""__li_source_path=""""
"""A member was added to a security-enabled"""
"""eventid=""""
]
Fields = [
"""({event_name}A member was added to a security-enabled [\w\s]+ group)"""
"""eventid="({event_code}47\d\d)""""
"""__li_source_path="({host}[^"]+)""""
"""__li_source_path="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
"""Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?).+?Account Domain:\s+({domain}[^\s]+).*Member"""
"""Logon ID:\s+({login_id}[^\s]+)\s+"""
"""Member:\s+Security ID:\s+(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\\s]+)\\+({account_name}.+?)|(?:.+?))\s+Account Name:"""
"""A member was added to a security-enabled ({group_type}\w+) group"""
"""(Information|Audit Success|Success Audit),({host}[\w.\-]+),"""
"""Member:.+?Account Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC.+?))\s+ Group:"""
"""Group:\s+Security ID:\s+({group_id}[^\s]+)"""
"""Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:"""
"""Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```