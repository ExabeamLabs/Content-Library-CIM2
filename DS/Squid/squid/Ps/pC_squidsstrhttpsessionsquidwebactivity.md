#### Parser Content
```Java
{
Name = "squid-s-str-http-session-squidwebactivity"
Vendor = "Squid"
Product = "Squid"
TimeFormat = "epoch_sec"
Conditions = [
"""<squid-web-activity-1>"""
]
Fields = [
"""({time}\d{10})\.\d{3}\s+({duration}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+({proxy_action}[^\s\/]+)\/({http_response_code}\d+)\s+({bytes_out}\d+)\s+({method}\S+)\s+({url}(\w+:\/+)?({web_domain}[^\s\/]+?)(:\d+|\/\S*?))\s+(?:-|({user}[\w\.\-]{1,40}\$?))\s+({hierarchy_code}[^\s\/]+)\/(?:-|({forwarded_host}\S+))\s+(?:-|({mime}\S+))"""
"""\d{10}\.\d{3}(\s+\S+){5}\s+(({protocol}\w+):\/+)?[^\s\/]*?({uri_path}\/[^\s\?]*?)({uri_query}\?[^\s]+)?\s"""
]
ParserVersion = "v1.0.0"


}
```