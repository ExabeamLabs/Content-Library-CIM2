#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-cef-alert-trigger-success-securitycenter
Vendor = Kaspersky
Product = Kaspersky Endpoint Security for Business
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """CEF"""
  """|KasperskyLab|SecurityCenter|"""
  """cs3Label=ProductVersion"""
  """destinationZoneURI="""
]
Fields = [
  """dhost=({dest_host}[^\s]+)\s*dst="""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """cs5=({task_name}.+?)\s\w+=.+?cs5Label=TaskName"""
  """cs5=({group_name}.+?)\s\w+=.+?cs5Label=SrcAdmGroupName"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """cs2=({product_name}.+?)\s\w+="""
  """dvchost=({host}.+?)\s\w+="""
  """dvc=({host}.+?)\s\w+="""
  """cs4=({alert_id}.+?)\s\w+="""
  """CEF:\s*\d\|([^\|]+\|){3}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
]
ParserVersion = "v1.0.0"


}
```