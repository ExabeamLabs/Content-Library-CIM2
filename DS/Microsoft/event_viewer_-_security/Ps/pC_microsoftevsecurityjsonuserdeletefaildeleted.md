#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-delete-fail-deleted"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A user account was deleted."""
]
Fields = [
"""({event_name}A user account was deleted)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4726)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^\"]+)"""
""""HostID":"({dest_host}({host}[\w\-.]+))"""
""""UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""Security_ID":"({user_sid}[^\"]+)"""
""""Source_Logon_ID":"({login_id}[^\"]+)"""
""""UserIDDst":"({account_name}({dest_user}[^\"]+))"""
]
ParserVersion = "v1.0.0"


}
```