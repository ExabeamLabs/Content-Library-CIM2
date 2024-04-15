#### Parser Content
```Java
{
Name = "cisco-iws-kv-http-session-info-1"
Vendor = "Cisco"
Product = "IronPort Web Security"
TimeFormat = "epoch_sec"
Conditions = [
"""Access_Logs_Syslog_exabeam:"""
"""Info:"""
]
Fields = [
"""({host}[^\s]+)\sAccess_Logs_Syslog_exabeam: Info: ({time}\d{10}\.\d{1,3})\s\S+\s({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s(NONE|({proxy_action}[^\s\/]+))(\/({http_response_code}\d+))?\s\S+\s({method}[^\s]+)\s(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({dest_port}\d+))?|({url}(\w+:\/+)?({web_domain}[^\/:]+)(:\d+)?({uri_path}\/[^\s?]*)?({uri_query}\?[^\s]*)?))\s(-|\"([^\\\"]+\\)?({user}[^\"@]+)(@({domain}[^\"]+))?\")\s\S+\s(-|({mime}[^\s]+))\s(\S+\s)<([^,]+,){22}\"(-|({category}[^\"]+))"""
]
ParserVersion = "v1.0.0"


}
```