#### Parser Content
```Java
{
Name = "symantec-wss-kv-http-session-nitroqueryresponse"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM|"""
"""nitroQuery_Response="""
]
Fields = [
"""\|McAfee\|ESM\|([^|]+?\|){2}({method}\w+)\s+({proxy_action}\w+)\s+({action}\w+)\|"""
"""\|McAfee\|ESM\|([^|]+?\|){2}({alert_name}[^|]+)\|"""
"""\Wrt=({time}\d{13})"""
"""\WdeviceDirection=({direction}\d+)"""
"""\Wdpt=({dest_port}\d+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsntdom=({web_domain}.*?)\s+(\w+=|$)"""
"""\Wsuser=({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
"""\WnitroResponse_Code=({http_response_code}\d+)"""
"""\WnitroCategory=({category}.*?)\s+(\w+=|$)"""
"""\WnitroQuery_Response=({action}.*?)\s+(\w+=|$)"""
"""\WnitroURL=({uri_path}[^=\?]*?)(\?({uri_query}.*?))?\s+(\w+=|$)"""
"""\Wduser=({user_agent}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```