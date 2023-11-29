#### Parser Content
```Java
{
Name = "darktrace-darktrace-cef-alert-trigger-success-darktrace"
 Vendor = "Darktrace"
 Product = "Darktrace"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [
  """CEF:"""
  """|Darktrace|DCIP|"""
 ]
 Fields = [
   """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\w+=""",
   """\|Darktrace\|DCIP\|[^\|]+\|\d+\|({alert_type}[^\/]*)\/\w+""",
   """"severityName":"({alert_severity}[^"]+)""""
   """\|Darktrace\|DCIP(\|[^\|]+){2}\|([^\|]+\/)?({alert_name}[^\|\/]*)\|({alert_severity}\d{1,2})\|""",
   """\|\d+\|({alert_type}[^\/]*)\/\w+""",
   """\/({alert_name}[^\|]*)\|\d""",
   """\s(dvc|src)=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s""",
   """\d{2}\s({host}[^\s]*)\s<""",
   """\|externalId=({alert_id}\d+)\s""",
   """\|Darktrace\|DCIP\|[^\|]+\|({category_id}[^\|]+?)\|""",
   """\s(dvc|s)host=(|({src_host}[^\s:]*))\s""",
   """\sdhost=(|({dest_host}[^\s]*))\s""",
   """\sdarktraceUrl=({url}[^\s]+)"""
   """\|({alert_severity}\d+)\|external"""
   """dvchost=[^\s]+?\s({email_address}[^\s@]+\@({email_domain}[^\s]+))?"""
   """"subject":"({email_subject}.+?)","\w+":""""
]
ParserVersion = "v1.0.0"


}
```