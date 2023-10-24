#### Parser Content
```Java
{
Name = "pan-ngfw-cef-http-session-url"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "epoch"
Conditions = [
"""|Palo Alto Networks|PAN-OS|"""
"""|url|THREAT|"""
]
Fields = [
"""\sdvc=({host}[^\s]+)"""
"""\sdvchost=({host}[\w\-.]+)"""
"""\sact=({action}[^\s]+)"""
"""\sproto=({protocol}[^\s]+)"""
"""\srt=({time}\d{13})"""
"""\Wrt="*({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser="?(|(({domain}[^\\\/="]*?)[\\\/]+)?({user}[\w\-.]+?))"?(\s+\w+=|\s*$)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\w+=|\s*$)"""
"""\sdpt=({dest_port}\d+)"""
"""\scs2=({category}[^=]+)(\s+\w+=|\s*$)"""
"""\srequestContext=(|({mime}.+?))(\s+\w+=|\s*$)"""
"""\srequest=\"({url}.+?)\"(\s+\w+=|\s*$)"""
"""\srequest=\"(\w+\\*:\/+)?[^\/\"=?]+({uri_path}\/[^?\s\"]*).*?\"(\s+\w+=|\s*$)"""
"""\srequest=\"[^\?\s\"=]*?({uri_query}\?.+?)\"(\s+\w+=|\s*$)"""
"""\srequest=\"(\w+\\*:\/+)?({web_domain}[^\/:\"\s]+).*?\"(\s+\w+=|\s*$)"""
"""\srequestMethod=({method}[^=\s]+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```