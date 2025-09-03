#### Parser Content
```Java
{
Name = "gtb-gtbi-cef-alert-trigger-success-gtb"
Vendor = "GTB"
Product = "GTB Technologies DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|GTB|GTBInspector|"""
  """externalId="""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdhost=(|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}.+?))(\s+\w+=|\s*$)"""
  """\Wdpt=({dest_port}\d+)"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wcs2=({protocol}[^=]+?)\s+\w+="""
  """\Wshost=(|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}.+?))(\s+\w+=|\s*$)"""
  """\Wspt=({src_port}\d+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)"""
  """\Wsuser=({email_address}[^=\s]+)"""
  """\Wsuser=[^=]*?<({email_address}[^<]+)>"""
  """\Wcs5=(|({alert_subject}.+?))(\s+\w+=|\s*$)"""
  """CEF[^\|]+?\|GTB\|GTBInspector\|[^\|]+?\|({alert_type}[^\|]+?)\|({alert_name}[^\|]+)\|({alert_severity}\d+)"""
  """\sduser=([\s\"]+suser=|[\s\"]*({target}.*?)[\s\"]*suser=)"""
]
ParserVersion = "v1.0.0"


}
```