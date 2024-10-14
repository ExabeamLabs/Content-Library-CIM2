#### Parser Content
```Java
{
Name = "juniper-ps-cef-http-session-success-webrequestcompleted"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|"""
"""|Web request completed|"""
"""WebRequest completed"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wresult\\=({http_response_code}\d+)"""
"""\Wsent\\=({bytes_out}\d+)"""
"""\Wreceived\\=({bytes_in}\d+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wsuser=(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\Wrequest=({url}(({protocol}[\w]+):\/+)?({web_domain}[^\s:\\\/]+)(:({dest_port}\d+)\/+)?({uri_path}\/[^\s\?]+)?({uri_query}\?[^\s]+)?)\s+([\w\\]+=|$)"""
"""\WrequestMethod=({method}[^\s]+)"""
"""\Wcn1=({category}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```