#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-success-devicecontrol
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Action="""
  """EventType=Device control;"""
  """ReportingName ="""
  """ComputerIPAddress="""
]
Fields = [
  """EventID=({alert_id}[\d]+);"""
  """EventTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """EventType=({alert_name}[^;]+);"""
  """Action=({action}[^;]+);"""
  """UserName =([^\\]+\\+)?({user}[^;]+);"""
  """ReportingName =({additional_info}.+?);"""
  """({additional_info}SubType=[^;]+)"""
  """ComputerName =({src_host}[^;]+);"""
  """ComputerIPAddress=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """ComputerDomain=({domain}[^;]+)"""
]
DupFields = [
  "action->alert_severity"
]
ParserVersion = "v1.0.0"


}
```