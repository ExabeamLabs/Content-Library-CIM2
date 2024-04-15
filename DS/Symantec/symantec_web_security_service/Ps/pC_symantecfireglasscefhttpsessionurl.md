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
"""cs6=\[([^,]+,\s){5}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s(-|non-interactive-user|({user}[^,]+))"""
"""\[[^]]+?(({action}OBSERVED)),\s({categories}({category}[^,;]+)[^,]*),\s(-|({referrer}.+?))\s*,\s({http_response_code}\d+),\s(-|({proxy_action}[^,]+)),\s({method}[^,]+),\s(-|({mime}[^,]+)),\s({protocol}[^,]+),\s({web_domain}[^,]+),\s({dest_port}\d+),\s({uri_path}[^\n]{1,4000}?)\s*,\s+(-|({uri_query}\?.*?))\s*,\s+(-|.+?),\s(none|-|({user_agent}[^\/,]+\/[\d\.]+[^\n]+?)|({=user_agent}[^,]+))?,\s(\d{1,3}\.){3}\d{1,3},\s({bytes_out}\d+),\s({bytes_in}\d+),\s"""
"""ICAP[^,]+,[^,]+,\s+ICAP[^,]+,[^,]+,\s+({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),\s"""
""",\sclient(,\s[^,]{1,4000}){22},\s(-|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\s({user_agent}Mozilla[^\n]+?),\s(\d{1,3}\.){3}\d{1,3},\s\d+,\s\d+""",
"""\s({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s(({domain}[^\s\\]+)\\)?({user}[^\s]+)\s(\S+\s){2}({action}OBSERVED)\s"({categories}({category}[^"]+)[^,"]*)"\s(-|({referrer}[^\s]+))\s({http_response_code}\d{1,100})\s(-|({proxy_action}[^\s]+))\s({method}[^\s]+)\s(-|({mime}[^\s]+))\s({protocol}[^\s]+)\s({web_domain}[^\s]+)\s({dest_port}\d{1,100})\s({uri_path}\S+?)?\s(-|({uri_query}\?[^\s]*?)?)\s\S+\s(none|-|"({user_agent}[^"]+)")\s(\d{1,3}\.){3}\d{1,3}\s({bytes_out}\d{1,100})\s({bytes_in}\d{1,100})\s(\S+\s){7,9}({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
]
ParserVersion = "v1.0.0"


}
```