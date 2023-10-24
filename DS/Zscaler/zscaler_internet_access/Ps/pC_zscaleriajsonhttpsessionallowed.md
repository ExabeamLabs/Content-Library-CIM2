#### Parser Content
```Java
{
Name = "zscaler-ia-json-http-session-allowed"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
Conditions = [
"""dlpeng="None""""
"""recordid=""""
"""saction=""""
"""url=""""
]
TimeFormat = "MMM dd HH:mm:ss yyyy z"
Fields = [
"""((::ffff:)?({host}[\w\-.]+)\s*")?\s*time="\w+\s({time}\w+\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d\s\w+)""""
"""urlcat="({category}[^"]+)"""
"""respsize="({bytes_in}\d+)"""
"""reqsize="({bytes_out}\d+)"""
"""saction="({action}[^"]+)"""
"""appname="({app}[^"]+)"""
"""c-ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""url="({url}(({protocol}[^:\\\/\s,]+):[\\\/]+)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^\\\/\s:,]+))(:\d+)?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s,]*)?)""""
"""dhostname="(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^"]+))""""
"""r-ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""csmethod="(NA|({method}[^"]+))"""
"""sc-status="(NA|({http_response_code}\d+))"""
"""cs\(User-Agent\)="(Unknown|({user_agent}[^"]+))"""
"""cs\(Referer\)="(Unknown|None|({referrer}[^"]+))"""
"""proto="({protocol}[^"]+)"""
"""url="({url}[^"]+)"""
"""reason="(Allowed|({failure_reason}[^"]+))"""
"""cs-username="({email_address}[^@"]+@[^\."]+\.[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```