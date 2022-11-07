#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-auditdam
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "epoch"
Conditions = [
  """CEF"""
  """|SecureSphere|"""
  """|Audit.DAM|"""
]
Fields = [
  """eventId=({alert_id}\d+)"""
  """cs2=({src_host}[^\s=]+?)\s\w+="""
  """\Wrt=({time}\d+)"""
  """cs1=({app}[^=]+?)\s\w+"""
  """deviceSeverity=({alert_severity}[^\s=]+?)\s\w+="""
  """cs3=({db_name}[^=]+?)\s\w+="""
  """cs4=(N\/A\s\()?({db_operation}\w+)"""
  """cs4=(N\/A\s*\(login\)|({db_query}.+?)\s\w+=)"""
  """ahost=({host}[^\s=]+?)\s\w+="""
  """src=({src_ip}[A-Fa-f.:\d]+)"""
  """dst=({dest_ip}[A-Fa-f.:\d]+)"""
  """dhost=({dest_host}.+?)\s\w+="""
  """spt=({src_port}\d+)"""
  """dpt=({dest_port}\d+)"""
  """cat=({service_name}[^=]+?)\s\w+="""
  """\Wduser=(({domain}[^\\\s@]+)\\+)?({user}[^\\\s@]+)\s+(\w+=|$)"""
  """proto=({protocol}[^\s=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```