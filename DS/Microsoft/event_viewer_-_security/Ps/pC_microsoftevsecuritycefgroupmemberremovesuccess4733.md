#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-group-member-remove-success-4733"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Snare|"""
"""Microsoft-Windows-Security-Auditing:4733"""
"""4733|A member was removed from a security-enabled"""
]
Fields = [
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
"""(\||\s)rt=({time}\d{13})"""
"""(\||\s)dvchost=({host}[\w\-.]+)\s*(\w+=|$)"""
"""(\||\s)dhost=({dest_host}[\w\-.]+)\s*(\w+=|$)"""
"""(\||\s)dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(\w+=|$)"""
"""(\||\s)Microsoft-Windows-Security-Auditing:\s*({event_code}\d+)"""
"""(\||\s)A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group"""
"""(\||\s)suser=(({domain}[^\\\s]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)"""
"""(\||\s)sntdom=({domain}.+?)\s*(\w+=|$)"""
"""(\||\s)suid=({login_id}[^\s]+)\s*(\w+=|$)"""
"""(\||\s)duser=({account_id}(?=[^\\]+\\)({sid_domain}[^\\]+?)\\({dest_user_sid}[^\\]+?)|(?:.+?))\s*(\w+=|$)"""
"""(\||\s)duid=\s*(-|({user_dn}CN=.+?({user_ou}OU.+?DC=[\w\-]+)))\s*dpriv="""
"""(\||\s)ad\.Group:Security_,ID=({group_id}[^\s]+)\s*(\w+=|$)"""
"""(\||\s)cs6=(({group_domain}[^\\]+?)\\+)?({group_name}[^\\]+?)\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```