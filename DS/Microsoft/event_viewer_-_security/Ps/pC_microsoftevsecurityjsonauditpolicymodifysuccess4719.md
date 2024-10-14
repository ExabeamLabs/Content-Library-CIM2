#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-audit-policy-modify-success-4719"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd HH:mm:ss Z"]
Conditions = [
""""EventID":4719"""
"""System audit policy was changed"""
]
Fields = [
    """({event_name}System audit policy was changed)""",
    """({event_code}4719)""",
    """"Hostname"+:"+({host}[^",]+)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\s*(\+|\-)[\d\:]+)?)"""",
    """"EventTime"+:"+({time}[^",]+)""",
    """"SubjectUserName"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"SubjectDomainName"+:"+({domain}[^"]+)""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """Category:(?:\\t|\\n|\\r|\s)*%*({audit_category}[^:]+?)(?:\\t|\\n|\\r|\s)*Subcategory:"""
    """Subcategory:(?:\\t|\\n|\\r|\s)*%*({sub_category}[^:]+?)(?:\\t|\\n|\\r|\s)*Subcategory GUID:""",
    """Changes:(?:\\t|\\n|\\r|\s)*%*({audit_policy_name}[^:"]+?)(?:\\t|\\n|\\r|\s)*"""",
  ]
ParserVersion = "v1.0.0"


}
```