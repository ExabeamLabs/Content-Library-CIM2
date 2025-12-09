#### Parser Content
```Java
{
Name = symantec-bcpa-str-network-traffic-fail-ssl
  ParserVersion = v1.0.0
  Conditions = [
"""PROXIED""",
"""- ssl"""
  ]
  Fields = ${BlueCoatParserTemplates.bluecoat-proxy.Fields}[
      """({action}OBSERVED|PROXIED|DENIED)\s+(?:-|"(-|none|({categories}({category}[^",;:]{1,30})[^"]*?))")\s+(?:-|({referrer}[^\s]+))\s+(?:-|({result_code}({http_response_code}\d+))?)\s+(?:-|({proxy_action}[^\s]+))\s+(?:-|unknown|({method}[^\s]+))\s+(?:-|({mime}[^\s]+))\s+((?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+)?(?:-|({protocol}[^\s]+))\s+(?:-|({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[^\s]+))\s+(?:-|({=dest_port}\d+))\s+(?:-|\/|({uri_path}[^\s]+))\s+(({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+)?(?:-|({uri_query}[^\s]+))\s+\S+\s+(?:-|"({user_agent}[^"]+?)\\?")\s+(?:-|({host}[^\s]+))\s+(?:-|({bytes_out}\d+))\s+(?:-|({bytes_in}\d+))\s+("*[^"]*"*\s+){3}(?:-|({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+""",
      """({action}OBSERVED|PROXIED|DENIED)\s+(?:-|\\?"(-|none|({categories}({category}[^",;:]{1,30})[^"]*?))\\?")\s+(?:-|({referrer}[^\s]+))\s+(?:-|({result_code}({http_response_code}\d+))?)\s+(?:-|({proxy_action}[^\s]+))\s+(?:-|unknown|({method}[^\s]+))\s+(?:-|({mime}[^\s]+))\s+(?:-|({protocol}[^\s]+))\s+(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[\w\-.]+))\s+(?:-|0|({dest_port}\d+))\s+(?:-|\/|({uri_path}\/[^\s]*?))\s+(?:-|({uri_query}[^\s]+))\s+\S+\s+(?:-|\\?"*({user_agent}[^"]+?)\\?"*)\s+(?:-|({host}[^\s]+))\s+(?:-|({bytes_out}\d+))\s+(?:-|({bytes_in}\d+))\s+("*[^"]*"*\s+){5}(?:-|({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+""",
      """({action}OBSERVED|PROXIED|DENIED)\s+(?:-|\\?"(none|({categories}({category}[^\\";]+)[^"]*?))\\?")\s+(?:-|({referrer}[^\s]+))\s+(?:-|({result_code}({http_response_code}\d+))?)\s+(?:-|({proxy_action}[^\s]+))\s+(?:-|unknown|({method}[^\s]+))\s+(?:-|({mime}[^\s]+))\s+(\S+\s)?(?:-|\\*"*({protocol}[^"\s]+))\\*"*\s+(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[\w\-.]+))\s+(?:-|0|({dest_port}\d+))\s+(?:-|\/|({uri_path}[^\s]*?))\s+(?:-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|(?:-?({uri_query}[^\s]+)))\s+\S+\s+(?:-|\\*"*({user_agent}[^"]+)\\*"*)\s+[-\s]*(?:-|({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?)\s+(?:-|({bytes_out}\d+)?)\s+(?:-|({bytes_in}\d+)?)""",
  ]


}
```