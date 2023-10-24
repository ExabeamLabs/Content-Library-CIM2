#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-audit-policy-modify-success-4719-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"event_id":4719""", """System audit policy was changed."""]
Fields = [
"""({event_name}System audit policy was changed)"""
""""@timestamp"\s*:\s*"({time}.+?)""""
""""(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-.]+?)""""
""""event_id"\s*:\s*({event_code}\d+)"""
""""(SubjectUserName)"\s*:\s*"({user}[\w\.\-]{1,40}\$?)\s*""""
""""(SubjectDomainName)"\s*:\s*"({domain}.+?)\s*""""
""""(SubjectLogonId|login_id)"\s*:\s*"({login_id}.+?)\s*""""
"""(\\t|\\n|\s)Category:(\\t|\\n|\s)*({audit_category}.+?)(\\t|\\n|\s)+Subcategory:"""
"""(\\t|\\n|\s)Subcategory:(\\t|\\n|\s)*({sub_category}.+?)(\\t|\\n|\s)+Subcategory GUID:"""
"""(\\t|\\n|\s)Changes:(\\t|\\n|\s)*({policy_name}.+?)(\\t|\\n|")"""
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```