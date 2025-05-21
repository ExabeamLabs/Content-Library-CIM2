#### Parser Content
```Java
{
Name = "symantec-wss-sk4-http-session-symantecwss"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""destinationServiceName =Symantec WSS"""
"""requestClientApplication=Broadcom WSS API"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s[^\s]+\s"""
"""cs6=.+?\d\d:\d\d:\d\d,\s*({host}[^,\s]+)"""
"""\s*({failure_reason}[^,]+),\s*({action}OBSERVED|PROXIED|DENIED),\s*(?:-|({category}[^,]+)),\s*(?:-|({referrer}[^,]+)),\s*(?:-|({http_response_code}\d+)),\s*(?:-|({proxy_action}[^,]+)),\s*(?:-|unknown|({method}[^,]+)),\s*(?:-|({mime}[^,]+)),\s*(?:-|({protocol}[^,]+)),\s*(?:-|({web_domain}[^,]+)),\s*(?:-|({dest_port}\d+)),\s*(?:-|({uri_path}[^,\s]+)),.+?,\s[^,]+,\s*(?:-|({user_agent}[^,]+)),\s*"""
"""cs6=\[.+({user_agent}Mozilla.+?),\s*(?:-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sproto=(-|({protocol}\d+))"""
"""\ssuid=({user_uid}[^\s]+)"""
"""\Wsuser=(({domain}[^\\\s]+)\\+)?(non-interactive-user|(-|anonymous|(?i)unauthenticated|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
"""\sapp=(-|({category}.+?))\s\w+="""
"""\sdhost=(-|({web_domain}.+?))\s\w+="""
"""\sdst=(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s\w+="""
"""\sflexString1=(-|({proxy_action}.+?))\s\w+="""
"""\ssrc=(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s\w+="""
"""\Wdproc=(|-|({process_name}.+?))(\s+\w+=|\s*$)"""
""",\s*(-|({additional_info}[^,]+)),?\s*(OBSERVED|PROXIED|DENIED)"""
"""(OBSERVED|PROXIED|DENIED)(,\s+[^,]+){66},\s+(-,\s)?(?:-|({transaction_id}[^,"\]]+))\]"""
]
ParserVersion = "v1.0.0"


}
```