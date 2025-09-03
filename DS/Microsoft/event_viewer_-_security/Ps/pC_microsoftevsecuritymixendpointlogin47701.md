#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-endpoint-login-4770-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""","EventID":"4770","""
"""<Data Name"""
"""'IpAddress'>"""
"""A Kerberos service ticket was renewed"""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_code}4770)"""
""""Activity":"({event_name}[^"]+)""""
""""Computer":"({host}[^"]+)""""
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name\\*=('|")TargetUserName('|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
"""<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
"""<Data Name\\*=('|")IpAddress('|")>(::\w+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
"""<Data Name\\*=('|")ServiceName('|")>({service_name}[^<]+)</Data>"""
"""<Data Name\\*=('|")ServiceName('|")>({dest_host}[\w\-.]+\$)</Data>"""
"""<Data Name\\*=('|")TicketOptions('|")>({ticket_options}[^<]+)</Data>"""
"""<Data Name\\*=('|")TicketEncryptionType('|")>({ticket_encryption_type}[^<]+)</Data>"""
]  
DupFields = [ "user_sid->dest_user_sid" , "domain->dest_domain", "user->dest_user" ]
ParserVersion = "v1.0.0"


}
```