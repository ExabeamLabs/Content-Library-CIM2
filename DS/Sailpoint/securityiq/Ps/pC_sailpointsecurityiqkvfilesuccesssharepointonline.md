#### Parser Content
```Java
{
Name = "sailpoint-securityiq-kv-file-success-sharepointonline"
Vendor = "Sailpoint"
Product = "SecurityIQ"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """| applicationtype : SharePoint Online |"""
  """actiontype : File """
]
Fields = [
  """creation_timestamp\s:\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3})"""
  """ipaddress\s:\s({host}[^|]+)\s\|"""
  """ipaddress\s:\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? \|"""
  """applicationtype\s:\s({app}[^|]+)\s\|"""
  """fileextension\s:\s({file_ext}[^|]+)\s\|"""
  """domain\s:\s({domain}[^|]+)\s\|"""
  """\spath\s:\s({file_dir}[^|]+)\s\|"""
  """userfullname\s:\s({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """objectname\s:\s({file_name}[^|]+) \|"""
  """actiontype\s:\sFile\s({operation}[^\s]+)(\s|\sExtended\s)\|"""
]
DupFields = [
  "operation->access"
]
ParserVersion = "v1.0.0"


}
```