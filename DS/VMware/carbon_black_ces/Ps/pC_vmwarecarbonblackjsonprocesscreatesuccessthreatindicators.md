#### Parser Content
```Java
{
Name = "vmware-carbonblack-json-process-create-success-threatindicators"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "epoch"
Conditions = [
  "threatIndicators"
  """eventType":"CREATE_PROCESS"""
  """ invoked """
  """parentPrivatePid":""""
]
Fields = [
  """"eventTime":({time}\d{13}),"""
  """deviceIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"deviceName":"(({domain}[^\\]+)\\+)?({src_host}[^"]+?)""""
  """"email":"(({domain}[^\\\s\"]+)\\+)?(HiveStreamingService|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """"eventType":"({alert_name}[^"]+)""""
  """"applicationName":"({process_name}[^"]+)""""
  """"targetPriorityType":"({alert_severity}[^"]+)""""
  """"shortDescription":"({additional_info}[^,]+)","""
  """"applicationPath":"({process_path}(({process_dir}[^\"]+?)[\\\/]+)?({process_name}[^\/\\\"]+))""""
  """"name":"({file_path}(\w:|\\\\)[^"]+)""""
  """"name":"({file_name}[^\\\/\"]+?(\.({file_ext}[^\"]+))?)""""
  """"name":"({file_dir}(\w:|\\\\)[^"]+)\\+(?:[^\\\"]+?)""""
  """"targetApp":\{[^\}]+\"sha256Hash\":\"({hash_sha256}[^"]+)""""
  """"targetApp":\{[^\}]+\"md5Hash\":\"({hash_md5}[^"]+)""""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```