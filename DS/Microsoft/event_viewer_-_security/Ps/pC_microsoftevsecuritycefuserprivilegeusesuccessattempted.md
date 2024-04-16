#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-attempted"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
""""eventID":"4674""""
"""An operation was attempted on a privileged object"""
]
Fields = [
""""systemTime":\"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""computer":\"({host}[\w\-.]+)"""
""""message":\"({event_name}[^\"]+?)\s*""""
""""eventID":\"({event_code}\d+)"""
""""eventRecordID":\"({event_id}\d+)"""
""""severityValue":\"({result}[^\"]+?)\s*""""
""""subjectUserSid":\"({user_sid}[^\s\"]+)"""
""""subjectLogonId":\"({login_id}[^\s\"]+)"""
""""objectServer":\"(-|({object_server}[^\s\"]+))"""
""""subjectUserName":\"(-|({user}[\w\.\-]{1,40}\$?))""""
""""subjectDomainName":\"(-|({domain}[^\s\"]+))""""
""""processName":\"(?: |({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))\s*""""
""""privilegeList":\"({privileges}[^\"]+?)\s*""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```