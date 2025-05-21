#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4769-4"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A Kerberos service ticket was requested"""
]
Fields = [
"""({event_name}A Kerberos service ticket was requested)"""
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""id":\d*({event_code}4769)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^"]+)"""
""""HostID":"({host}[^"]+)"""
""""UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""Service_Name":"({service_name}[^"]+)"""
""""Service_Name":"({dest_host}[\w\-.]+\$)"""
""""CommandID":"({result_code}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```