#### Parser Content
```Java
{
Name = "eset-es-cef-alert-trigger-success-eventtype"
Vendor = "ESET"
Product = "ESET Endpoint Security"
TimeFormat = "dd-MMM-yyyy HH:mm:ss"
Conditions = [
  """event_type":""""
  """occured":""""
  """source_uuid":""""
]
Fields = [
  """occured":"({time}[^,\"]+)"""
  """({host}[^\s]+)\sERAServer\s"""
  """(?:,|\")(threat_name|event)":\"({alert_name}[^",]+)"""
  """(threat_type|protocol)\":\"({alert_type}[^,"]+)"""
  """severity":"({alert_severity}[^,\"]+)"""
  """event_type":"({additional_info}[^,"]+)"""
  """scanner_id":"({additional_info}[^,"]+)"""
  """object_uri":".+?(?i)(users|documents and settings)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\\/]"""
  """username":"(?:({domain}[^\"\\]*?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """object_uri":"\w+:(\/)+({malware_url}[^,\"]+)"""
  """ipv4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """source_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """target_address":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"processname":"({process_path}[^\"]+\\({process_name}[^\"]+))""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```