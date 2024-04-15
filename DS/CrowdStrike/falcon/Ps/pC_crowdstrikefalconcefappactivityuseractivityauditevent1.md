#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-activity-useractivityauditevent-1"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
"""CEF:"""
"""|CrowdStrike|FalconHost|"""
"""cat=UserActivityAuditEvent"""
]
Fields = [
"""\Wrt=({time}\d{10})"""
"""\Wduser=({user}[^=@]+?)(@({domain}[^@]+?))?\s*(\w+=|$)"""
"""CrowdStrike\|([^|]+\|){3}({operation}[^|]+)"""
"""({app}FalconHost)"""
]
DupFields = [
"domain->email_domain"
]
ParserVersion = "v1.0.0"


}
```