#### Parser Content
```Java
{
Name = "cisco-securewebapp-csv-http-session-info"
Vendor = "Cisco"
Product = "Cisco Secure Web Appliance"
TimeFormat = "epoch_sec"
Conditions = [
""" SOC_ExabeamPOC_accesslogs: Info: """
]
Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+SOC_ExabeamPOC_accesslogs: Info:\s*({time}\d{10})\.\d+\s+\d+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(NONE|({proxy_action}[^\s\/]+))\/({http_response_code}\d+)\s+\d+\s+({method}\S+)\s+(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?(({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({web_domain}[^\\\/\s:,"]+))?(:({dest_port}\d+))?({uri_path}\/[^\s\?]*)?({uri_query}\?[^\s]*?)?)),?\s+(\S+\s+\S+\s+(-|({mime}\S+))\s+.+?<(-|({category}[^,">]+)))?"""
]
DupFields = [
"dest_ip->web_domain"
]
ParserVersion = "v1.0.0"


}
```