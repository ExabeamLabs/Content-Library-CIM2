#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-endpoint-login-4769-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""EventID":"4769""""
"""<Data Name"""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""EventID":"({event_code}\d+)"""
""""Computer":"({host}[^"]+)"""
"""<Data Name\\*=('|")Status('|")>({result_code}[^<]+)</Data>"""
"""<Data Name\\*=('|")ServiceName('|")>({dest_host}[\w\-.]+\$)</Data>"""
"""<Data Name\\*=('|")ServiceName('|")>({service_name}[^<]+)</Data>"""
"""<Data Name\\*=('|")TicketOptions('|")>({ticket_options}[^<]+)</Data>"""
"""<Data Name\\*=('|")TicketEncryptionType('|")>({ticket_encryption_type}[^<]+)</Data>"""
"""<Data Name\\*=('|")TargetUserName('|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^<]+))?</Data>"""
"""<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
"""<Data Name\\*=('|")IpAddress('|")>(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [ "domain->dest_domain", "user->dest_user" ]
ParserVersion = "v1.0.0"


}
```