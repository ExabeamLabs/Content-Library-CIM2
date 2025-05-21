#### Parser Content
```Java
{
Name = "zscaler-ia-kv-dns-response-success-allow"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = ["MMM dd HH:mm:ss yyyy","MMM  dd HH:mm:ss yyyy"]
Conditions = [
"""department="""
"""location="""
"""deviceowner="""
"""devicehostname="""
"""dns_reqtype="""
]
Fields = [
"""reqaction=({result}[^\s]+)"""
"""datetime=\w{1,3}\s+({time}\w{1,3}\s+\d+\s\d\d:\d\d:\d\d\s\d{4})"""
"""user=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s"""
"""dns_reqtype=({dns_query_type}[^\s]+)"""
"""durationms=({duration}\d+)"""
"""category=(Miscellaneous or Unknown|({category}[^\=]+?)\s+\w+=)"""
"""dns_resp=((?i)NOERROR|NXDOMAIN|SERVFAIL|REFUSED|({dns_response}[^\s]+))"""
"""dns_resp=({dns_response_code}((?i)NOERROR|NXDOMAIN|SERVFAIL|REFUSED))"""
"""dns_req=({dns_query}[^\s]+)"""
"""reqrulelabel=({rule}[^\=]+?)\s+\w+="""
"""srv_dip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""srv_dport=({dest_port}\d+)\s+"""
"""department=({department}[^\=]+?)\s+\w+="""
"""location=({location}[^\=]+?)\s+\w+="""
"""deviceowner=(NA|({owner_id}[^\s]+))"""
"""devicehostname=({host}[\w\-.]+?)\s*(\w+=|"*$)"""
"""clt_sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```