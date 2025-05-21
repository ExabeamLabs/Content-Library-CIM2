#### Parser Content
```Java
{
Name = "cisco-fp-kv-alert-trigger-success-threatname"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """Protocol:"""
  """ThreatName:"""
  """-430005:"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[\w.\-]+)?"""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """\sSrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sDstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sSrcPort:\s*({src_port}\d+)"""
  """\sDstPort:\s*({dest_port}\d+)"""
  """\sProtocol:\s*({protocol}[^,]+?)(,|\s*$)"""
  """\sUser:\s*(Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(,|\s*$)"""
  """\sFileAction:\s*({alert_type}[^,]+?)(,|\s*$)"""
  """\sFilePolicy:\s*({alert_name}[^,]+?)(,|\s*$)"""
  """\sFileName:\s*({file_path}({file_dir}[^,]*?[\\\/]+)?({file_name}[^,\\\/]*?(\.({file_ext}\w+))?))(,|\s*$)"""
  """\sFileSize:\s*({bytes}\d+)"""
  """\sFileType:\s*({file_type}[^,]+?)(,|\s*$)"""
  """\sFileSHA256:\s*({hash_sha256}[^,]+?)(,|\s*$)"""
  """\sFileDirection:\s*({direction}[^,]+?)(,|\s*$)"""
  """\sClient:\s*({user_agent}[^,]+?)(,|\s*$)"""
  """\sDeviceUUID:\s*({device_id}[^,]+?)(,|\s*$)"""
  """ThreatScore:\s+({alert_severity}\d+)"""
]
ParserVersion = "v1.0.0"


}
```