#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-memberadded"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy H:mm:ss a"
Conditions = [
""""Message":"A member was added to a security-enabled """
""""InstanceId":"""
""""EntryType""""
]
Fields = [
"""({event_name}A member was added to a security-enabled [\w\s]+ group)"""
""""MachineName":"({host}[^."]+)"""
""""TimeGenerated":"({time}[^"]*)"""
""""InstanceId":"({event_code}[^"]+)"""
""""Message":"A member was added to a security-enabled ({group_type}[^\s]+) group."""
""""6":"({user}[^"]+)"""
""""5":"({user_sid}[^"]+)"""
""""7":"({domain}[^"]+)"""
""""8":"({login_id}[^"]+)"""
""""2":"({group_name}[^"]+)"""
""""3":"({group_domain}[^"]+)"""
""""1":"({account_id}[^"]+)"""
""""0":"({user_dn}[^"]+)"""
""""0":"CN=.*,({user_ou}OU=.+?DC=.+?[^"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```