#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-anaccountfailedtologon"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""An account failed to log on"""
]
Fields = [
"""({event_name}An account failed to log on)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4625)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^"]+)"""
""""HostID":"({host}[^"]+)"""
""""UserIDSrc":"({user}[\w\.\-]{1,40}\$?)"""
""""Security_ID":"({user_sid}[^"]+)"""
""""Logon_Type":"({login_type}\d+)"""
""""ObjectID":"({auth_package}[^"]+)"""
""""Status":"({failure_reason}[^"]+)"""
""""Sub_Status":"({result_code}[^"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```