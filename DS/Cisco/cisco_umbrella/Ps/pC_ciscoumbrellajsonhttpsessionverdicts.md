#### Parser Content
```Java
{
Name = "cisco-umbrella-json-http-session-verdicts"
Product = "Cisco Umbrella"
Vendor = "Cisco"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""""Type":"UmbrellaIntelligentProxyLogs"""
"""Verdict_s"""
"""TenantId"""
"""statusCode_s"""
]
Fields = [
"""TimeGenerated"+:"+({time}[^"]+)"""
""""Computer"+:"+({host}[^"]+)?"+,"""
""""Referer_s"+:"+({referrer}[^"]+)?"+,"""
""""userAgent_s"+:"+({user_agent}[^"]+)?"+,"""
""""Verdict_s"+:"+({action}[^"]+)?"+,"""
""""Categories_s"+:"+({category}[^,"]+)?"+,"""
""""Categories_s"+:"+({categories}[^"]+)?"+,"""
""""responseSize_s"+:"+({bytes_out}\d+)?"+,"""
""""requestSize_s"+:"+({bytes_in}\d+)?"+,"""
""""statusCode_s"+:"+({http_response_code}\d+)?"+,"""
""""ContentType_s"+:"+({mime}[^"]+)?"+,"""
""""URL_s"+:"+({url}[^"]+)?"+,"""
""""ExternalIP_s"+:"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+,"""
""""InternalIP_s"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+,"""
"""URL_s"+:"+\s*[^"]+?({uri_query}\?[^\s"]+)"""
"""URL_s"+:"+\s*(?:-|\w+:\/+)({web_domain}[^\s\/"]+)"""
""""+URL_s"+:"+.[^"]+?:\/*([^\/"]+)\/({uri_path}[^\s"]+)"""
]
ParserVersion = "v1.0.0"


}
```