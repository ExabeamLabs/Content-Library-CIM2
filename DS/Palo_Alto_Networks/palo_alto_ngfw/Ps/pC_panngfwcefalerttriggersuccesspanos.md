#### Parser Content
```Java
{
Name = "pan-ngfw-cef-alert-trigger-success-panos"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["epoch", "MMM dd yyyy HH:mm:ss Z", "MMM dd yyyy HH:mm:ss"]
Conditions = [
  """|Palo Alto Networks|PAN-OS|"""
  """|spyware|THREAT|"""
]
Fields = [
  """\sdvchost=({host}[\w\-.]+)"""
  """\Wrt="*({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d(\s\w{3})?)"*\s+(\w+=|$)"""
  """\srt=({time}\d{13})\s+(\w+=|$)"""
  """\srequest="({malware_url}[^"]+)""""
  """({alert_type}spyware)"""
  """\scat=({alert_name}[^=]+)\s+(\w+=|$)"""
  """\sPanOSThreatID="*({alert_name}[^"=\(]+?)(\s*\([^\)]+?\)?)"*\s+\w+="""
  """\sshost=({src_host}[^=]+)\s+(\w+=|$)"""
  """\sdhost=({dest_host}[^=]+)\s+(\w+=|$)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|$)"""
  """\sdeviceSeverity=({alert_severity}\d+)\s"""
  """\|spyware\|THREAT\|(Unknown|({alert_severity}[^\|]+))"""
  """\seventId=({alert_id}\d+)\s+(\w+=|$)"""
  """\sapp=({threat_category}[^=]+)\s+(\w+=|$)"""
  """\ssuser="*((({domain}[^\\\/="]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"*"""
  """\sproto=({protocol}[^=]+?)\s+\w+="""
  """\sact=({action}[^=]+?)\s+\w+="""
  """\sspt=({src_port}\d+)"""
  """\sdpt=({dest_port}\d+)"""
  """\scs1="*({rule}[^="]+?)"*\s+\w+="""
  """\scs4=({src_network_zone}[^\s]+)""",
  """\scs5=({dest_network_zone}[^\s]+)""",
  """deviceInboundInterface=({src_interface}[^\s]+)""",
  """deviceOutboundInterface=({dest_interface}[^\s]+)""",
  """deviceExternalId=({serial_num}\d+)""",
  """\sapp=(not-applicable|({network_app}[^=]+?))\s\w+="""
	"""sourceTranslatedAddress=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
  """destinationTranslatedAddress=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
]
DupFields = [ "alert_name->alert_subject" ]
ParserVersion = "v1.0.0"


}
```