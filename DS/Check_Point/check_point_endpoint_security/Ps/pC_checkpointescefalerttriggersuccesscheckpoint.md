#### Parser Content
```Java
{
Name = "checkpoint-es-cef-alert-trigger-success-checkpoint"
Vendor = "Check Point"
Product = "Check Point Endpoint Security"
TimeFormat = "epoch"
Conditions = [
  """|Check Point|New Anti Virus|"""
  """cs4Label="""
]
Fields = [
  """({host}[\w.\-]+) CEF:"""
  """\Wcp_severity=(?:|({alert_severity}.+?))(\s+\w+=|\s*$)"""
  """\Wrt=({time}\d{13})"""
  """\Worigin=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Woriginsicname=(?:|({user_ou}.+?))(\s+\w+=|\s*$)"""
  """\Wcontract_name=(?:|({alert_name}.+?))(\s+\w+=|\s*$)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wcs(3|6)=(?:|({alert_type}.+?))(\s+\w+=|\s*$)"""
  """\Wcs4=(?:|({alert_name}.+?))(\s+\w+=|\s*$)"""
  """\Wcs4Label=Protection Name cs4=({alert_name}.+?)(\s+\w+=|\s*$)"""
  """\WflexString2=(?:|({additional_info}.+?))(\s+\w+=|\s*$)"""
  """\WdestinationDnsDomain=(?:|({malware_url}.+?))(\s+\w+=|\s*$)"""
  """\Wspt=({src_port}\d+)"""
  """\Wdpt=({dest_port}\d+)"""
  """\Wfname=(|({file_name}.+?(\.({file_ext}\w+))?))(\s+\w+=|\s*$)"""
  """\Wrequest=(|({malware_url}.+?))(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```