#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-group-member-remove-success-4733-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
""""eventID":"4733""""
"""Security Enabled"""
""" Group Member Removed"""
]
Fields = [
""""systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""computer":"({host}[\w\-.]+)"""
""""message":"({event_name}[^"]+?)\s*""""
""""eventID":"({event_code}\d+)"""
""""eventRecordID":"({event_id}\d+)"""
""""severityValue":"({result}[^"]+?)\s*""""
"""Security Enabled ({group_type}[^\s]+) Group Member"""
""""memberSid":"(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^"\s]+?))\s*""""
""""targetUserName":"({group_name}[^"\s]+?)\s*""""
""""targetDomainName":"({group_domain}[^"\s]+?)\s*""""
""""targetSid":"({group_id}[^"\s]+?)\s*""""
""""subjectUserSid":"({user_sid}[^"\s]+?)\s*""""
""""subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""""
""""subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*""""
""""subjectLogonId":"({login_id}[^"\s]+?)\s*""""
]
ParserVersion = "v1.0.0"


}
```