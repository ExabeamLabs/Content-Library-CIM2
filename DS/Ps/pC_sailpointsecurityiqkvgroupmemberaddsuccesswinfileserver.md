#### Parser Content
```Java
{
Name = "sailpoint-securityiq-kv-group-member-add-success-winfileserver"
Conditions = [
"""| applicationtype : Windows File Server (Agent) |"""
"""actiontype : Member Added"""
]
DupFields = [
"host->dest_host"""
"domain->account_used_domain"""
"user->account"""
"user_sid->account_name"""
]
ParserVersion = "v1.0.0"


}
```