#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-dns-request-success-256"
Vendor = "Microsoft"
Product = "Event Viewer - DNSServer"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<Data Name""","""'QNAME'>""","""'QTYPE'>""","""'Flags'>"""
]
Fields = [
"""TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)"""
"""Computer>({host}.+?)<\/Computer>"""
"""EventID>({event_code}\d+)<\/EventID>"""
"""Execution ProcessID\\*='({process_id}\d+)"""
"""<Data Name\\*='XID'>({query_id}\d+)"""
"""ThreadID\\*='({thread_id}[^\']+)"""
"""<Data Name\\*='InterfaceIP'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""<Data Name\\*='Source'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""<Data Name\\*='Port'>({src_port}\d+)"""
"""<Data Name\\*='QNAME'>({dns_query}[^<]+)\.?<\/Data>"""
"""<Data Name\\*='QTYPE'>({dns_query_type}.+?)<\/Data>"""
"""<Data Name\\*='Flags'>({dns_query_flags}.+?)<\/Data>"""
"""<Data Name\\*='BufferSize'>({bytes}\d+)<\/Data>"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```