#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-auditdam
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["epoch", "MMM dd yyyy HH:mm:ss"]
Conditions = [
  """CEF"""
  """|SecureSphere|"""
  """|Audit.DAM|"""
]
Fields = [
  """eventId=({alert_id}\d+)"""
  """cs2=({src_host}[^\s=]+?)\s\w+="""
  """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)"""
  """\Wrt=({time}\d{13})"""
  """cs1=({app}[^=]+?)\s\w+"""
  """deviceSeverity=({alert_severity}[^\s=]+?)\s\w+="""
  """cs3=({db_name}[^=]+?)\s\w+="""
  """cs4=(N\/A\s\()?({db_operation}\w+)"""
  """cs4=(N\/A\s*\(login\)|({db_query}.+?)\s\w+=)"""
  """ahost=({host}[^\s=]+?)\s\w+="""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """dhost=({dest_host}.+?)\s\w+="""
  """spt=({src_port}\d+)"""
  """dpt=({dest_port}\d+)"""
  """cat=({service_name}[^=]+?)\s\w+="""
  """\Wduser="?\s*(({domain}[^\\\s@]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?\s*"?\s+(\w+=|$)"""
  """proto=({protocol}[^\s=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```