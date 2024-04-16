#### Parser Content
```Java
{
Name = "infoblox-bddi-cef-dns-request-success-mcafee"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|McAfee|ESM|"""
"""Infoblox_NIOS DNS Query|"""
"""Query\="""
]
Fields = [
"""({host}\S+) CEF:"""
"""CEF:([^\|]*\|){5}({event_name}[^\|]+)"""
"""\Wrt=({time}\d{13})"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wspt=({src_port}\d+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wproto=({protocol}\S+)"""
"""\W(\^_|_)?Query\\=({dns_query}.+?)s*([\w\\]+=|$)"""
"""\WType_Name\\=({dns_query_type}.+?)\s*([\w\\]+=|$)"""
"""\WnitroRequest_Type=(-|({dns_query_flags}.+?))\s*([\w\\]+=|$)"""
]
ParserVersion = "v1.0.0"


}
```