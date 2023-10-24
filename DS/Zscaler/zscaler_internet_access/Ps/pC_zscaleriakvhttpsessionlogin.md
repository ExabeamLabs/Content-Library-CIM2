#### Parser Content
```Java
{
Name = "zscaler-ia-kv-http-session-login"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "MMM  dd HH:mm:ss yyyy"
Conditions = [
"""login="""
"""cip="""
"""eurl="""
"""urlsupercat="""
"""action="""
]
Fields = [
"""epochtime=({time}\d+)"""
"""ehost=({host}[^\s]+)"""
""""time=\w+\s+({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)"""
"""login=({email_address}({user}[\w\.\-]{1,40}\$?)@[^@\s"]+)"""
"""(\W|")reason=({proxy_action}[^="]+?)("|\s+\w+=)"""
"""(\s|")action=({action}[^="]+?)("|\s+\w+=)"""
"""(\W|")reqmethod=(NA|({method}[^"=]+?))("|\s+\w+=)"""
"""(\W|")cip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\W|")sip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""(\W|")proto=({protocol}[^="]+?)("|\s+\w+=)"""
"""(\W|")eurl=((\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({web_domain}[^\/:"]+))(:({dest_port}\d+))?({uri_path}[^?"\s]+)?(\?({uri_query}[^,]+))?","""
"""(\W|")eurl=({url}[^="]+)("|\s\w+=)"""
"""(\W|")urlsupercat=({category}[^+=]+?)("|\s+\w+=)"""
"""(\W|")ua=(Unknown|({user_agent}[^"=]+?))("|\s+\w+=)"""
"""reqsize=({bytes_out}\d+)"""
"""respsize=({bytes_in}\d+)"""
"""respcode=({http_response_code}\d+)"""
"""(\W|")ereferer=(None|({referer}[^="]+?))\s*(\w+=|"|$)"""
""""appname=({app}[^"]+)"""
""""appclass=({app_group}[^"]+)"""
""""dlpdict=(None|({dlp_dict}[^"]+))"""
""""dlpeng=(None|({dlp_eng}[^"]+))"""
""""location=(None|({location}[^"]+))"""
""""dept=(None|({department}[^"]+))"""
""""malwarecat=(None|({malware_category}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```