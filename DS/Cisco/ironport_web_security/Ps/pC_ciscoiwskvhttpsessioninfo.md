#### Parser Content
```Java
{
Name = "cisco-iws-kv-http-session-info"
Vendor = "Cisco"
Product = "IronPort Web Security"
TimeFormat = "epoch_sec"
Conditions = [
"""W3C_Logs_Syslog_Exabeam:"""
"""Info:"""
]
Fields = [
"""({host}[^\s]+)\sW3C_Logs_Syslog_Exabeam: Info: ({time}\d{10})\.\d{1,3}\s\S+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s(-|\"([^\\\"]+\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\"]+))?\")\s({src_port}\d+)\s(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s({=dest_port}\d+)\s({url}(\w+:\/+)?({web_domain}[^\/:]+)(:\d+)?({uri_path}\/[^\s?]*)?({uri_query}\?[^\s]*)?)\s(\S+\s){3}(-|\"({user_agent}[^\"]+)\")\s\S+\s({method}[^\s]+)\s({http_response_code}\d+)\s(\S+\s){2}(NONE|({proxy_action}[^\s]+))"""
]
ParserVersion = "v1.0.0"


}
```