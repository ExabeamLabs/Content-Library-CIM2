#### Parser Content
```Java
{
Name = "symantec-fireglass-cef-http-session-url"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""destinationServiceName =Symantec WSS"""
"""OBSERVED"""
"""http"""
]
Fields = [
"""cs6=\[([^,]+,\s){5}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s(-|non-interactive-user|({user}[\w\.\-]{1,40}\$?))"""
"""\[[^]]+?(({action}OBSERVED)),\s({categories}({category}[^,;]+)[^,]*),\s(-|({referrer}.+?))\s*,\s({http_response_code}\d+),\s(-|({proxy_action}[^,]+)),\s({method}[^,]+),\s(-|({mime}[^,]+)),\s({protocol}[^,]+),\s({web_domain}[^,]+),\s({dest_port}\d+),\s({uri_path}[^\n]{1,4000}?)\s*,\s+(-|({uri_query}\?.*?))\s*,\s+(-|.+?),\s(none|-|({user_agent}[^\/,]+\/[\d\.]+[^\n]+?)|({=user_agent}[^,]+))?,\s(\d{1,3}\.){3}\d{1,3

}
```