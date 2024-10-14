#### Parser Content
```Java
{
Name = "forcepoint-wsg-kv-http-session-websensewsg"
Vendor = "Forcepoint"
Product = "Websense Security Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" websense_wsg|v"""
]
Fields = [
"""({host}[\w.\-]+)\s+websense_wsg\|v"""
"""websense_wsg\|([^\^]+\^){3}(?:-|({action}[^\^]+))\^(?:-|({protocol}[^\^]+))\^(?:-|({http_response_code}\d+)?)\^[^\^]+\^(?:-|[^\^]*?=(({domain}[^\^\\\/=]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\^(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\^(?:-|({=src_port}\d+)?)\^(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\^(?:-|({=dest_port}\d+)?)\^(?:-|({web_domain}[^\^]+))\^[^\^]+\^(?:-|({bytes_out}\d+)?)\^(?:-|({bytes_in}\d+)?)\^([^\^]+\^){9}(?:-|({method}[^\^]+))\^(?:-|({mime}[^\^]+))\^[^\^]+\^(?:-|({user_agent}[^\^]+))\^[^\^]+\^(?:-|({url}[^\^]+?))\s*(\^|$)"""
]
ParserVersion = "v1.0.0"


}
```