#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-authentication-sucess-4769-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""__li_source_path="""
"""A Kerberos service ticket was requested"""
"""eventid="4769""""
]
Fields = [
"""({event_name}A Kerberos service ticket was requested)"""
"""__li_source_path="({host}[^"]+)""""
"""({event_code}4769)"""
"""Account Name:\s+({user}[^@]+)@({domain}[\w._\-]+)"""
"""Service Name:\s+(?: |({dest_host}\S+\$))\s+Service ID"""
"""Service Name:\s+(?: |({service_name}\S+))\s+Service ID"""
"""Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Failure Code:\s+({result_code}[\w]+)"""
"""Ticket Encryption Type:\s+({ticket_encryption_type}[^\s]+)"""
"""Ticket Options:\s+({ticket_options}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```