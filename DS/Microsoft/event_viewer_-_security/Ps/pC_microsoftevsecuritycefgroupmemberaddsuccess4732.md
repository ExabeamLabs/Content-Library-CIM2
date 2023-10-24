#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-group-member-add-success-4732"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
""""eventID":"4732""""
"""Security Enabled"""
"""Group Member Added"""
]
Fields = [
""""systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""computer":"({host}[\w\-.]+)"""
""""message":"({event_name}[^"]+?)\s*""""
""""eventID":"({event_code}\d+)"""
""""eventRecordID":"({event_id}\d+)"""
""""severityValue":"({result}[^"]+?)\s*""""
""""targetSid":"({group_id}[^"\s]+?)\s*""""
""""targetUserName":"({group_name}[^"\s]+?)\s*""""
""""targetDomainName":"({group_domain}[^"\s]+?)\s*""""
""""subjectUserSid":"({user_sid}[^"\s]+?)\s*""""
""""subjectUserName":"({user}[\w\.\-]{1,40}\$?)\s*""""
""""subjectDomainName":"({domain}[^"\s]+?)\s*""""
""""subjectLogonId":"({login_id}[^"\s]+?)\s*""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```