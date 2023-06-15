#### Parser Content
```Java
{
Name = mcafee-dlp-cef-printer-activity-success-printingprotection
Vendor = "McAfee"
Product = "McAfee DLP Endpoint"
TimeFormat = "epoch"
Conditions = [
  """McAfee|Data Loss Prevention"""
  """|DLP: Printing Protection|"""
]
Fields = [
  """(\s|\|)rt=({time}\d{13})\s+([\w\.-]+=|$)"""
  """\d\d:\d\d\s+({host}[^\s]+)\sCEF:"""
  """(\s|\|)cs2=({dest_host}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)cs2=\\+.+?(\\+({printer_name}.+?))\s+([\w\.-]+=|$)"""
  """(\s|\|)dhost=({dest_host}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+([\w\.-]+=|$)"""
  """(\s|\|)duser=({user}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)dntdom=({domain}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)fname=({object}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)fsize=({bytes}\d+)\s+([\w\.-]+=|$)"""
  """(\s|\|)({operation}Printing)"""
]
ParserVersion = "v1.0.0"


}
```