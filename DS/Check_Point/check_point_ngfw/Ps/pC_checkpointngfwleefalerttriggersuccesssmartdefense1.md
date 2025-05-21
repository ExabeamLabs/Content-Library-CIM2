#### Parser Content
```Java
{
Name = checkpoint-ngfw-leef-alert-trigger-success-smartdefense-1
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Conditions = ["""SmartDefense""","""action=""","""reason=""","""ifdir="""]
  Fields = [
  """\Worigin=({host}[\w\-.]+)(\s+\w+:?=|\s*$)"""
  """\Woriginsicname=(|({user_ou}.+?))(\s+\w+=|\s*$)"""
  """\Wcat=({alert_type}.+?)(\s+\w+:?=|\s*$)"""
  """\WdevTime=({time}\d{10})"""
  """\Wreason=({additional_info}.+?)(\s+\w+:?=|\s*$)"""
  """\WsrcPort=({src_port}\d+)"""
  """\Wservice=({dest_port}\d+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wproto=({protocol}.+?)(\s+\w+:?=|\s*$)"""
  """\Wloguid=\{({log_uid}.+?)\}"""
  """\scat=({alert_source}.+?)(\s+\w+:?=|\s*$)"""
  """\Waction=({result}[^\s]+)"""
  """\Wreason=({alert_name}[^\.=]+?)(\.|\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```