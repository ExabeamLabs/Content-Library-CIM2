#### Parser Content
```Java
{
Name = "damballa-fs-leef-alert-trigger-success-failsafe"
 Vendor = "Damballa"
 Product = "Damballa Failsafe"
 TimeFormat = "epoch"
 Conditions = [
   """|Damballa|Failsafe|"""
 ]
 Fields = [
   """devTime=({time}\d{13})""",
   """LEEF:1.0\|Damballa\|Failsafe\|[^\|]+\|({alert_type}[^\|]+)""",
   """LEEF:1.0\|Damballa\|Failsafe\|[^\|]+\|({alert_name}[^\|]+)""",
   """fsIndustryName =({alert_name}[^=]+?)(\s|\\t)+\w+=""",
   """fsIncidentSeverity=({alert_severity}[^=]+?)(\s|\\t)+\w+=""",
   """\tshost=({src_host}(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[^\t]+)""",
   """\tsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """\tdomain=({domain}[^\t]+)""",
   """\texternalId=({alert_id}[^\t]+)""",
   """\tdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
 ]
 ParserVersion = "v1.0.0"


}
```