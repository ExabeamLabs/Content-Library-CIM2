#### Parser Content
```Java
{
Name = "symantec-fireglass-kv-http-session-urlcategories"
Vendor = "Symantec"
Product = "Symantec Fireglass"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""", url_categories:"""
""", top_level_url_host:"""
""", top_level_url_scheme:"""
""", malicious:"""
]
Fields = [
"""@timestamp:\s*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""\Whost:\s*({host}[^\s,]+)"""
"""\Wtop_level_url_scheme:\s*({protocol}[^,]+)"""
"""\Wusername:\s*({email_address}[^,\s]+)"""
"""\Wdestination_ip:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wurl_port:\s*({dest_port}\d+)"""
"""\Wurl_host:\s*({web_domain}[^,]+)"""
"""\Wresponse_status_code:\s*({http_response_code}\d+)"""
"""\Wurl:\s*"({url}[^",]+)"""
"""\Wurl:\s*"*(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s"]+)"""
"""\Wurl:\s*"*(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))"""
"""\Wrequest_method:\s*({method}[^,]+)"""
"""\Wcontent_type:\s*({mime}[^,]+)"""
"""\Waction:\s*({action}[^,]+)"""
"""\Wurl_categories:\s*\[(|({categories}[^\]]+))"""
"""\Wurl_categories:\s*\[(|({category}[^,;\]]+))"""
"""\Wsource_ip:\s*({src_translated_ip}[A-Fa-f:\d.]+)"""
"""\Woriginal_source_ip:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wuser_agent:\s*({user_agent}[^,]+)"""
"""\Wreferer_url:\s*({referrer}[^,\}]+)"""
"""\Wmalicious:\s*({result}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```