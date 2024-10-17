#### Parser Content
```Java
{
Name = "cisco-securewebapp-csv-http-session-qradarlogging"
Vendor = "Cisco"
Product = "Cisco Secure Web Appliance"
TimeFormat = "epoch_sec"
Conditions = [
"""QRadarLogging: Info:"""
]
Fields = [
"""Info:\s*({time}\d{10})\.\d+\s+\d+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(NONE|({proxy_action}[^\s\/]+))\/({http_response_code}\d+)\s+({bytes_out}\d+)\s+({method}\S+)\s+(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)(:\d+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))\s(-|({domain}[^s]+))\s.*?\s({mime}[^\s]+)"""
"""Info:\s*({time}\d{10})\.\d+\s+\d+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(NONE|({proxy_action}[^\s\/]+))\/({http_response_code}\d+)\s+({bytes_out}\d+)\s+({method}\S+)\s+(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)(:\d+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))(\s+(-|"{1,20}(({domain}[^\\\s"]+)\\+)?({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^\\\s"@]+)"{1,20})\s+[^\s\/]+\/+(-|({=web_domain}[^\s\/]+))\s+(-|({mime}\S+))\s+.+?<(-|({category}[^",>]+)).+?dst\s+(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+dstPort\s+({=dest_port}\d+))?"""
"""Info:\s.*?\s({src_ip}\d+.\d+.\d+.\d+)\s({proxy_action}[^\/]+)\/({http_response_code}\d+)\s\d+\s({method}[^\s]+)\s*({url}.+?\.([^\s]*\.)[^\s]+)"""
""""(-|({category}[^"]+?))",([^,]+?,){19}->"""
"""dst\s(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\sdstPort\s(-|({=dest_port}\d+))"""
]
ParserVersion = "v1.0.0"


}
```