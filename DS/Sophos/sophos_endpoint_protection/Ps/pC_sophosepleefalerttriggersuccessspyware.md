#### Parser Content
```Java
{
Name = sophos-ep-leef-alert-trigger-success-spyware
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LEEF:1.0|Sophos|Enterprise Console|"""
  """|Viruses/spyware"""
]
Fields = [
  """EventID=({alert_id}[\d]+)"""
  """devTime=({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})"""
  """usrName =[^\\]*\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """LEEF:[^|]*\|Sophos\|Enterprise Console\|[^|]*\|({alert_name}[^|]*)\|"""
  """ReportingName =({alert_type}.+?)\s+(\w+=|$)"""
  """ComputerName =({src_host}.+?)\s+(\w+=|$)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """ActionName =({result}.*?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```