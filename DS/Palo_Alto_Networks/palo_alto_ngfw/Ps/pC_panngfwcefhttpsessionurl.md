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
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""suser="?(|(({domain}[^\\\/="]*?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?(\s+\w+=|\s*$)"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\w+=|\s*$)"""
"""dpt=({dest_port}\d+)"""
"""cs2=({category}[^=]+)(\s+\w+=|\s*$)"""
"""requestContext=(|({mime}.+?))(\s+\w+=|\s*$)"""
"""request=\"({url}.+?)\"(\s+\w+=|\s*$)"""
"""request=\"(\w+\\*:\/+)?[^\/\"=?]+({uri_path}\/[^?\s\"]*).*?\"(\s+\w+=|\s*$)"""
"""request=\"[^\?\s\"=]*?({uri_query}\?.+?)\"(\s+\w+=|\s*$)"""
"""request=\"(\w+\\*:\/+)?({web_domain}[^\/:\"\s]+).*?\"(\s+\w+=|\s*$)"""
"""requestMethod=({method}[^=\s]+?)\s+\w+="""
"""cs4=({src_network_zone}[^\s]+)"""
"""cs5=({dest_network_zone}[^\s]+)"""
"""deviceInboundInterface=({src_interface}[^\s]+)"""
"""deviceOutboundInterface=({dest_interface}[^\s]+)"""
"""deviceExternalId=({serial_num}\d+)"""
"""\sapp=(not-applicable|({network_app}[^=]+?))\s\w+="""
"""sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
"""destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
"""\sdvc=({device_name}[^\s]+)"""
"""\sdvchost=({device_name}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```