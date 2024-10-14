#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-anaccountwassuccessfullyloggedon"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""An account was successfully logged on"""
]
Fields = [
"""({event_name}An account was successfully logged on)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4624)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^"]+)"""
""""HostID":"({host}[\w\-.]+)"""
""""UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""Security_ID":"({user_sid}[^"]+)"""
""""Source_Logon_ID":"({login_id}[^"]+)"""
""""Logon_Type":"({login_type}\d+)"""
""""ObjectID":"({auth_package}[^"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```