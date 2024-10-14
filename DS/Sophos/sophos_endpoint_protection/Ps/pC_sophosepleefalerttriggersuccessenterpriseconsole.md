#### Parser Content
```Java
{
Name = sophos-ep-leef-alert-trigger-success-enterpriseconsole
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LEEF:1.0|Sophos|Enterprise Console|"""
  """|Web """
]
Fields = [
  """EventID=({alert_id}[\d]+)"""
  """devTime=({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})"""
  """LEEF:[^|]*\|Sophos\|Enterprise Console\|[^|]*\|({alert_name}[^|]*)\|"""
  """ReportingName =({alert_type}.+?)\s+(\w+=|$)"""
  """usrName =[^\\]*\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """ComputerName =({src_host}.+?)\s+(\w+=|$)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"
},	

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
  """Action=({result}[^;]+);"""
  """UserName =([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?);"""
  """ReportingName =({additional_info}.+?);"""
  """({additional_info}SubType=[^;]+)"""
  """ComputerName =({src_host}[^;]+);"""
  """ComputerIPAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """ComputerDomain=({domain}[^;]+)"""
]
DupFields = [
  "result->alert_severity"
]
ParserVersion = "v1.0.0"


}
```