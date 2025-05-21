#### Parser Content
```Java
{
Name = "zscaler-ia-leef-http-session-nss"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = ["MMM dd yyyy HH:mm:ss z"]
Conditions = [
"""|Zscaler|NSS|"""
"""|cat="""
]
Fields = [
"""devTime=({time}\w+ \d+ \d+ \d+:\d+:\d+ [^=]+?)(?:\\|\s+\w+=|\|)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""usrName =({email_address}[^\s@]+@[^=\|]+?)\s*(\\t)?(\w+=|\|)"""
"""cat=({action}[^\s\|\\]+)"""
"""policy=({proxy_action}[^=\|\\]+?)\s*(\w+=|$|\|)"""
"""urlcategory=({categories}({category}[^=\|]+?))\s*(\\t)?(\w+=|$|\|)"""
"""url=({url}[^\s\|]+)(\\t)?"""
"""url=(\w+:\/{2})?[^\/\s\|]+({uri_path}\/[^?\s]+)(\\t)?"""
"""url=[^=|?]+({uri_query}\?[^\s\|]+)\s(\\t)?"""
"""url=(?:[^:?]+:\/+)?({web_domain}[^\/:\s\|]+)(:({dest_port}\d+))?(\\t)?"""
"""srcBytes=({bytes_out}\d+)"""
"""dstBytes=({bytes_in}\d+)"""
"""appproto=({protocol}[^=\|]+?)\s*(\\t)?(\w+=|$|\|)"""
"""appname=({app}[^=]+?)\s*(\\t)?(\w+=|$|\|)"""
"""useragent=(Unknown|({user_agent}[^=\|]+?))\s*(\\t)?(\w+=|$|\|)"""
"""respcode=({http_response_code}\d+)"""
"""reqmethod=(NA|({method}[^=\|]+?))\s*(\\t)?(\w+=|$|\|)"""
"""fileclass=(None|({mime}[^=\|]+?))\s*(\\t)?(\w+=|$|\|)"""
"""referer=(None|({referrer}[^\s\|]+?))\s*(\\t)?(\w+=|$|\|)"""
"""riskscore=({risk_level}\d+)"""
]
ParserVersion = "v1.0.0"


}
```