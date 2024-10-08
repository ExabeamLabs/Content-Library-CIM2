#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-audit-policy-modify-success-4719"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" 4719 """
"""System audit policy was changed"""
"""AUDIT_SUCCESS"""
]
Fields = [
"""({event_name}System audit policy was changed)"""
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s+AUDIT_SUCCESS"""
"""({event_code}4719)"""
"""\sAccount Name:\s*({user}[\w\.\-]{1,40}\$?)\s+Account Domain"""
"""\sAccount Domain:\s*({domain}[^\s]+)"""
"""\sLogon ID:\s*({login_id}[^\s]+)"""
"""\sCategory:\s*({audit_category}.+?)\s+Subcategory:"""
"""\sSubcategory:\s*({sub_category}.+?)\s+Subcategory GUID:"""
"""\sChanges:\s*({audit_policy_name}.+?)\s*(\w+:|$)"""
]
ParserVersion = "v1.0.0"


}
```