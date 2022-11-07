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
  """FullFilePath=C:\\Users\\({user}[^\\]+)"""
  """ThreatName =({alert_name}[^;]+);"""
  """UserName =([^\\]+\\+)?(SYSTEM|({user}[^;]+))"""
  """ComputerName =({src_host}[^;]*);"""
  """ComputerIPAddress=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """FullFilePath=({file_path}[^;]+?)\s*(;|$)"""
  """FullFilePath=({malware_url}[^;]+\\({malware_file_name}[^;]+))"""
  """Status=({alert_severity}[^;]+)"""
  """FullFilePath=(?:\w:)?[^;]+?\\(?:[^\\]+\\){4}({file_name}[^\\]+)\\"""
]
ParserVersion = "v1.0.0"


}
```