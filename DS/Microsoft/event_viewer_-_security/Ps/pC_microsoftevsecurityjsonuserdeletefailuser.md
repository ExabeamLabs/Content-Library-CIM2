#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-delete-fail-user"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A user account was locked out."""
]
Fields = [
"""({event_name}A user account was locked out)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id\":\d*({event_code}4740)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({src_domain}[^\"]+)"""
""""HostID":"({host}[\w\-.]+)"""
""""UserIDSrc":"({src_user}[^\"]+)"""
""""Security_ID":"({user_sid}[^\"]+)"""
""""Source_Logon_ID":\"({login_id}[^\"]+)"""
""""UserIDDst":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
DupFields = [
"src_domain->domain"
]
ParserVersion = "v1.0.0"


}
```