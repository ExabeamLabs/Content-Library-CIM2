#### Parser Content
```Java
{
Name = "symantec-wss-sk4-http-session-denied"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""destinationServiceName =Symantec WSS"""
""", DENIED,"""
]
Fields = [
"""cs6=\[([^,]+,\s){5}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s(-|non-interactive-user|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""dvchost=(-|({host}[^\s]+))\s\w+="""
"""\[[^]]+?,\s(-|({failure_reason}[^,]+)),\s(({action}DENIED)),\s({categories}({category}[^,;]+)[^,]*),\s(-|({referrer}.+?))\s*,\s({http_response_code}\d+),\s(-|({proxy_action}[^,]+)),\s({method}[^,]+),\s(-|({mime}[^,]+)),\s({protocol}[^,]+),\s({web_domain}[^,]+),\s({dest_port}\d+),\s({uri_path}[^\n]+?)\s*,\s+(-|({uri_query}\?.*?))\s*,\s+(-|.+?),\s(none|-|({user_agent}[^\/,]+\/[\d\.]+[^\n]+?)|({=user_agent}[^,]+))?,\s(\d{1,3}\.){3}\d{1,3},\s({bytes_out}\d+),\s({bytes_in}\d+),\s"""
"""ICAP[^,]+,[^,]+,\s+ICAP[^,]+,[^,]+,\s+({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),\s"""
""",\sclient(,\s[^,]+){22},\s(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\s({user_agent}Mozilla[^\n]+?),\s(\d{1,3}\.){3}\d{1,3},\s\d+,\s\d+"""
"""DENIED(,\s+[^,]+){25},\s+(-,\s)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(,\s+[^,]+){28},\s+(-|({src_host}[\w.-]+))"""
"""DENIED(,\s+[^,]+){2},\s+({http_response_code}\d+),"""
""",\s*(-|({additional_info}[^,]+)),?\s*DENIED"""
"""(OBSERVED|PROXIED|DENIED)(,\s+[^,]+){66},\s+(-,\s)?(?:-|({transaction_id}[^,"\]]+))"""
]
ParserVersion = "v1.0.0"


}
```