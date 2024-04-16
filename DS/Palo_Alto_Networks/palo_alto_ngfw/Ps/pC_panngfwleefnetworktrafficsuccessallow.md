#### Parser Content
```Java
{
Name = pan-ngfw-leef-network-traffic-success-allow
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """LEEF:"""
  """|Palo Alto Networks|PAN-OS Syslog Integration|"""
  """|allow|"""
]
Fields = [
  """\s({host}[\w\.-]+)\s+LEEF:"""
  """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)"""
  """\|Type=({event_category}\w+)\|"""
  """\|Subtype=({subtype}\w+)\|"""
  """\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\|"""
  """\|dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\|"""
  """\|srcPostNAT=(0\.0\.0\.0|({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\|"""
  """\|dstPostNAT=(0\.0\.0\.0|({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\|"""
  """\|RuleName =({rule}[^\|]*?)\|"""
  """\|usrName =(|((({domain}[^\|\\]+)\\)?({user}[\w\.\-]{1,40}\$?)))\|"""
  """\|SourceUser=(|((({src_domain}[^\|\\]+)\\)?({src_user}[^\|\\]+)))\|"""
  """\|DestinationUser=(|((({dest_domain}[^\|\\]+)\\)?({dest_user}[^\|\\]+)))\|"""
  """\|SourceZone=({src_network_zone}[^\|]+)\|"""
  """\|DestinationZone=({dest_network_zone}[^\|]+)\|"""
  """\|srcPort=(0|({src_port}\d+))\|"""
  """\|dstPort=(0|({dest_port}\d+))\|"""
  """\|srcPostNATPort=(0|({src_translated_port}\d+))\|"""
  """\|dstPostNATPort=(0|({dest_translated_port}\d+))\|"""
  """\|proto=({protocol}[^\|]+)"""
  """\|totalBytes=({bytes}[\d.]+)\|"""
  """\|srcBytes=({bytes_out}[\d.]+)\|"""
  """\|dstBytes=({bytes_in}[\d.]+)\|"""
  """\|URLCategory=({category}[^\|]+)"""
  """\|Direction=({direction}[\w-]+)\|"""
  """\|SessionEndReason=({result_reason}[^\|]+)"""
  """\|action=({action}\w+)\|"""
  """\|SourceLocation=({src_location}[^\|]+)\|""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```