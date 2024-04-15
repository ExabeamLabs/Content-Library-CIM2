#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-audit-policy-modify-success-4719"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4719"""
"""System audit policy was changed"""
]
Fields = [
    """({event_name}System audit policy was changed)""",
    """({event_code}4719)""",
    """"Hostname"+:"+({host}[^",]+)""",
    """"EventTime"+:"+({time}[^",]+)""",
    """"SubjectUserName"+:"+({user}[^"]+)""",
    """"SubjectDomainName"+:"+({domain}[^"]+)""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """Category:(?:\\t|\\n|\\r|\s)*({audit_category}[^:]+?)(?:\\t|\\n|\\r|\s)*Subcategory:"""
    """Subcategory:(?:\\t|\\n|\\r|\s)*({sub_category}[^:]+?)(?:\\t|\\n|\\r|\s)*Subcategory GUID:""",
    """Changes:(?:\\t)*({audit_policy_name}[^"]+)""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```