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
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|$)"""
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
]
DupFields = [ "alert_name->alert_subject" ]
ParserVersion = "v1.0.0"


}
```