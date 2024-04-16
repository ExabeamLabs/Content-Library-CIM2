#### Parser Content
```Java
{
Name = "infowatch-dlp-cef-http-session-success-mailinbrowser"
Vendor = "InfoWatch"
Product = "InfoWatch DLP"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Mail in Browser|"""
"""|DLP|DLP TM"""
]
Fields = [
"""\Wact=({action}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wrt=({time}\d{13})"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsntdom=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(\s+[\w\.]+=|\s*$)"""
"""\Wduser=({web_domain}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wrequest=({url}(\w+:\/\/)?[^\/]+?({uri_path}\/[^\?\s]*?)({uri_query}\?.*?)?)(\s+[\w\.]+=|\s*$)"""
"""\Wdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)"""
"""\Wdvc=({host}.+?)(\s+[\w\.]+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```