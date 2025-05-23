#### Parser Content
```Java
{
Name = "pan-ngfw-cef-http-session-url"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["epoch", "MMM dd yyyy HH:mm:ss"]
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
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser="?(|(({domain}[^\\\/="]*?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?(\s+\w+=|\s*$)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\w+=|\s*$)"""
"""\sdpt=({dest_port}\d+)"""
"""\scs2=({category}[^=]+)(\s+\w+=|\s*$)"""
"""\srequestContext=(|({mime}.+?))(\s+\w+=|\s*$)"""
"""\srequest=\"({url}.+?)\"(\s+\w+=|\s*$)"""
"""\srequest=\"(\w+\\*:\/+)?[^\/\"=?]+({uri_path}\/[^?\s\"]*).*?\"(\s+\w+=|\s*$)"""
"""\srequest=\"[^\?\s\"=]*?({uri_query}\?.+?)\"(\s+\w+=|\s*$)"""
"""\srequest=\"(\w+\\*:\/+)?({web_domain}[^\/:\"\s]+).*?\"(\s+\w+=|\s*$)"""
"""\srequestMethod=({method}[^=\s]+?)\s+\w+="""
"""\scs4=({src_network_zone}[^\s]+)"""
"""\scs5=({dest_network_zone}[^\s]+)"""
"""deviceInboundInterface=({src_interface}[^\s]+)"""
"""deviceOutboundInterface=({dest_interface}[^\s]+)"""
"""deviceExternalId=({serial_num}\d+)"""
"""\sapp=(not-applicable|({network_app}[^=]+?))\s\w+="""
"""sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
"""destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
]
DupFields = ["host->device_name"]
ParserVersion = "v1.0.0"


}
```