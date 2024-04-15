#### Parser Content
```Java
{
Name = "zscaler-ia-kv-dns-response-success-allow"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""department="""
"""location="""
"""deviceowner="""
"""devicehostname="""
"""dns_reqtype="""
]
Fields = [
"""reqaction=({action}[^\s]+)"""
"""datetime=\w+\s({time}\w+\s+\d+\s\d+:\d+:\d+\s\d+)"""
"""user=(({email_address}[^@]+@[^\s]+)|({user}[^\s]+))\s"""
"""dns_reqtype=({dns_query_type}[^\s]+)"""
"""durationms=({duration}\d+)"""
"""category=(Miscellaneous or Unknown|({category}[^\=]+?)\s+\w+=)"""
"""dns_resp=((?i)NOERROR|NXDOMAIN|SERVFAIL|REFUSED|({dns_response}[^\s]+))"""
"""dns_resp=({dns_response_code}((?i)NOERROR|NXDOMAIN|SERVFAIL|REFUSED))"""
"""dns_req=({dns_query}[^\s]+)"""
"""reqrulelabel=({rule}[^\=]+?)\s+\w+="""
"""srv_dip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""srv_dport=({dest_port}\d+)\s+"""
"""department=({department}[^\=]+?)\s+\w+="""
"""location=({location}[^\=]+?)\s+\w+="""
"""deviceowner=(NA|({device_owner}[^\s]+))"""
"""devicehostname=({host}[^\"]+?)\s*(\w+=|"*$)"""
"""clt_sip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```