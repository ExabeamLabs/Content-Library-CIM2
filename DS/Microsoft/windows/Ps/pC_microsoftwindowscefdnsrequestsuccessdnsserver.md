#### Parser Content
```Java
{
Name = "microsoft-windows-cef-dns-request-success-dnsserver"
Vendor = "Microsoft"
Product = "Windows"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|DNS Server|"""
"""app=DNS Query"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wapp=({event_code}DNS Query)"""
"""\Wrequest=({dns_query}.+?)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wcs1=({dns_query_type}.+?)\s+(\w+=|$)"""
"""\Wcs5=({dns_query_flags}.+?)\s+(\w+=|$)"""
"""\Wproto=({protocol}.+?)\s+(\w+=|$)"""
"""\WdeviceSeverity=({dns_response_code}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```