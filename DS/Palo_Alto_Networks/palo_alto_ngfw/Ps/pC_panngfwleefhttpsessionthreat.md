#### Parser Content
```Java
{
Name = "pan-ngfw-leef-http-session-threat"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """LEEF:"""
  """|Palo Alto Networks|PAN-OS Syslog Integration|"""
  """|cat=THREAT|"""
  """ubtype=url|"""
]
Fields = [
  """\|\s*ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """({host}[\w\.-]+)\s+LEEF:"""
  """usrName =({domain}[^\\\|]+)\\({user}[^\s\|]+)"""
  """\|src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?((\|\w+=|\s*$))"""
  """\|srcPort=({src_port}\d+)((\|\w+=|\s*$))"""
  """\|dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?((\|\w+=|\s*$))"""
  """\|dstPort=({dest_port}\d+)((\|\w+=|\s*$))"""
  """\|action=({action}[^\|]+)((\|\w+=|\s*$))"""
  """\|URLCategory=({category}[^\|]+)((\|\w+=|\s*$))"""
  """\|SourceUser=(({domain}[^\|]+)\\)?({user}[^\|]+)((\|\w+=|\s*$))"""
  """\|DestinationUser=(({domain}[^\|]+)\\)?({user}[^\|]+)((\|\w+=|\s*$))"""
  """\|usrName =(({domain}[^\|]+)\\)?({user}[^\|]+)((\|\w+=|\s*$))"""
  """\|proto=({protocol}[^\|]+)((\|\w+=|\s*$))"""
  """\|Miscellaneous=\"*({url}[^\s]*?)(\"+\|\w+=|\"+\s*$|\s*$)"""
  """\|Miscellaneous=\"*({web_domain}[^\/\s\"]+?)(:\d+|\/|\")[^\s]*?(\"+\|\w+=|\"+\s*$|\s*$)"""
  """\|Miscellaneous=\"*([^\/\s\"]+)({uri_path}\/[^\s\"\?]+)[^\s]*?(\"+\|\w+=|\"+\s*$|\s*$)"""
  """\|Miscellaneous=\"*([^\s\?\"]+)(|({uri_query}\?[^\s]+?))(\"+\|\w+=|\"+\s*$|\s*$)"""
  """\|ContentType=({mime}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```