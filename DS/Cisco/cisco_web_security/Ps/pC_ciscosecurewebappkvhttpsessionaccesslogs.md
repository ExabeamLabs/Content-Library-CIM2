#### Parser Content
```Java
{
Name = "cisco-securewebapp-kv-http-session-accesslogs"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Web Security"
  TimeFormat = "epoch_sec"
  Conditions = [ """ Exabeam_access_logs_export: Info: """ ]
    Fields = [
      """\s({host}[\w\-.]+)\sExabeam_access_logs_export: Info:"""
      """Exabeam_access_logs_export: Info:\s*({time}\d{10})\.\d+\s+\d+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(NONE|({proxy_action}[^\s\/]+))\/({http_response_code}\d+)\s+\d+\s+({method}\S+)\s+(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({url}(({protocol}[^:\\\/\s,\"]+):[\\\/]+)?(({=dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({web_domain}[^\\\/\s:,\"]+))?(:({=dest_port}\d+))?({uri_path}\/[^\s\?]*)?({uri_query}\?[^\s]*?)?)),?\s+(\"\S+\s+\S+\s+(-|({mime}\S+)))?"""
      """\s<\"\w+_([^,]*,){22}\"\s*(-|({category}[^\"]+?))\s*\""""
      """Exabeam_access_logs_export: Info: ([^\s]+\s){7}\"[^\"]+?\"\s[^\s\/]+\/(-|({web_domain}[^\s]+))\s"""
   ]


}
```