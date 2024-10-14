#### Parser Content
```Java
{
Name = "microsoft-iis-xml-http-session-6200"
Vendor = "Microsoft"
Product = "Microsoft IIS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<EventID>6200</EventID>"""
"""<Provider Name""",
"""'Microsoft-Windows-IIS-Logging'"""
]
Fields = [
"""<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'"""
"""<Computer>({host}[^<]+?)<"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Data Name\\*='cs-method'>(-|({method}[^<]+?))<"""
"""<Data Name\\*='sc-status'>(-|({http_response_code}\d+))<"""
"""<Data Name\\*='cs-uri-stem'>(-|\/|({uri_path}[^<]+?))<"""
"""<Data Name\\*='cs-uri-query'>(-|({uri_query}[^<]+?))<"""
"""<Data Name\\*='c-ip'>(::1|127.0.0.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)<"""
"""<Data Name\\*='s-ip'>(::1|127.0.0.1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)<"""
"""<Data Name\\*='s-port'>(-|({dest_port}\d+?))<"""
"""<Data Name\\*='sc-bytes'>({bytes_out}\d+)"""
"""<Data Name\\*='cs-bytes'>({bytes_in}\d+)"""
"""<Data Name\\*='csUser-Agent'>(-|({user_agent}[^<]+?))<"""
"""<Data Name\\*='cs-host'>(-|({web_domain}[^<]+?))<"""
"""<Keywords>({result}[^<]+)<"""
"""<Data Name\\*='s-computername'>(-|({src_host}[^<]+?))<"""
"""<Data Name\\*='cs-username'>(-|(0#\.f\|ww\|)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^.\d<]+)?)<"""
"""<Data Name\\*='cs-username'>(-|((0#\.f\|ww\|)|(0#\.w\|))?(((({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({email_address}[^@]+@[^.<]+?\.[^<]+)))<"""
]
ParserVersion = "v1.0.0"


}
```