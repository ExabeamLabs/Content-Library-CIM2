#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-json-dns-request-success-qname"
Vendor = "Microsoft"
Product = "Event Viewer - DNSServer"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""<leaf>"""
"""Microsoft-Windows-DNSServer"""
""""QNAME":""""
""""QTYPE":""""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+)\sMicrosoft-Windows-DNSServer"""
"""\"EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\"EventId\":({event_code}\d+)"""
"""\"ExecutionProcessID\":({process_id}\d+)"""
"""\"XID\":\"({query_id}\d+)"""
"""\"ExecutionThreadID\":({thread_id}\d+)"""
"""\"InterfaceIP\":\"(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\"Source\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"Port\":\"({src_port}\d+)"""
"""\"QNAME\":\"({dns_query}[^\",]+)\.\","""
"""\"QTYPE\":\"({dns_query_type}[^\"]+)"""
"""\"Flags\":\"({dns_query_flags}[^\"]+)"""
"""\"BufferSize\":\"({bytes}\d+)"""
"""\"Domain\":\"((?i)NT AUTHORITY|({domain}[^\"]+))"""
"""\"AccountName\":\"((?i)SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
"""\"UserID\":\"({user_sid}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```