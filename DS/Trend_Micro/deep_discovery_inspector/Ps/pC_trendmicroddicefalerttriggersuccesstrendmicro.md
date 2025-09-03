#### Parser Content
```Java
{
Name = "trendmicro-ddi-cef-alert-trigger-success-trendmicro"
Vendor = "Trend Micro"
Product = "Deep Discovery Inspector"
TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
Conditions = [
"""CEF:"""
"""|Trend Micro|Deep Discovery Inspector|"""
"""hostSeverity="""
"""peerIp="""
]
Fields = [
"""CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
"""CEF:([^\|]*\|){5}({alert_type}[^\|]+)\|"""
"""\WeventId=({alert_id}\d+)"""
"""\Wdvc=({host}.+?)(\s+\w+=|\s*$)"""
"""\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
"""\Wrt=({time}\w+\s+\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)"""
"""\Wshost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^\s]+))"""
"""\Wdhost=({malware_url}[^\s]+)"""
"""\Wapp=({app}.+?)(\s+\w+=|\s*$)"""
"""\Wdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdpt=({src_port}\d+)"""
"""\Wsrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wspt=({dest_port}\d+)"""
"""\Wact=({result}.+?)(\s+\w+=|\s*$)"""
"""\Wsmac=({src_mac}.+?)(\s+\w+=|\s*$)"""
"""\WmalType=((?i)(OTHERS)|({alert_type}.+?))(\s+\w+=|\s*$)"""
"""\WmalType=((?i)(OTHERS)|({alert_name}.+?))(\s+\w+=|\s*$)"""
"""\WruleName =({alert_name}.+?)(\s+\w+=|\s*$)"""
"""\WcompressedFileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))(\s+\w+=|\s*$)"""
"""\WhostSeverity=({alert_severity}.+?)(\s+\w+=|\s*$)"""
"""\WpeerIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s+\w+=|\s*$)"""
"""\WinterestedIp=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```