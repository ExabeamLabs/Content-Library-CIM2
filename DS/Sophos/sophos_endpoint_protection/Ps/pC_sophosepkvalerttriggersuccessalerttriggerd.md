#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-success-alerttriggerd
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ThreatName ="""
  """ComputerIPAddress="""
]
Fields = [
  """;\s+EventID=({alert_id}[\d]+);"""
  """EventTime=({time}[\d\- :]+);"""
  """ThreatType=({alert_type}[^;]+);"""
  """FullFilePath=C:\\Users\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """ThreatName =({alert_name}[^;]+);"""
  """UserName =([^\\]+\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """ComputerName =({src_host}[^;]*);"""
  """ComputerIPAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """FullFilePath=({file_path}[^;]+?)\s*(;|$)"""
  """FullFilePath=({malware_url}[^;]+\\({malware_file_name}[^;]+))"""
  """Status=({alert_severity}[^;]+)"""
  """FullFilePath=(?:\w:)?[^;]+?\\(?:[^\\]+\\){4}({file_name}[^\\]+)\\"""
]
ParserVersion = "v1.0.0"


}
```