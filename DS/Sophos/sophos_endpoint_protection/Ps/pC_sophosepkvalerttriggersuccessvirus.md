#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-success-virus
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """EventType=Virus"""
  """ReportingName ="""
  """ComputerIPAddress="""
]
Fields = [
  """;\s+EventID=({alert_id}[\d]+);"""
  """;\s*EventTime=({time}[\d\- T\+:]+);"""
  """;\s*EventType=({alert_type}[^;]+);"""
  """;\s*Name =({alert_name}[^;]+);"""
  """;\s*UserName =([^\\]+\\+)?({user}[\w\.\-]{1,40}\$?);"""
  """;\s*Action=({alert_severity}[^;]+);"""
  """;\s*({additional_info}SubType=[^;]+)"""
  """;\s*ComputerName =({src_host}[^;]+);"""
  """;\s*ComputerIPAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """;\s*BlockedSite=({malware_url}[^;]+?)\s*(;|$)"""
  """;\s*Category=(|({alert_name}[^;]+?))\s*(;|$)"""
  """;\s*ReferringURL=({additional_info}[^;]+?)\s*(;|$)"""
]
ParserVersion = "v1.0.0"


}
```