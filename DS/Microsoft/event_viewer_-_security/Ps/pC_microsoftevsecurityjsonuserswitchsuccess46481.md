#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-switch-success-4648-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A logon was attempted using explicit credentials."""
]
Fields = [
"""({event_name}A logon was attempted using explicit credentials)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4648)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^"]+)"""
""""HostID":"({host}[\w\-.]+)"""
""""UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""UserIDDst":"({dest_user}[^"]+)"""
""""Security_ID":"({user_sid}[^"]+)"""
""""Source_Logon_ID":"({login_id}[^"]+)"""
""""Process_Name":"({process_name}[^"]+?)""""
""""PID":"({process_id}[^"]+)"""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```