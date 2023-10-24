#### Parser Content
```Java
{
Name = "vmware-carbonblack-json-network-traffic-success-connectionto"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "epoch"
Conditions = [
  """threatIndicators":"""
  """ connection to """
  """sourceAddress":""""
  """destinationServiceName =CB Defense"""
]
Fields = [
  """"eventTime":({time}\d{13})"""
  """"deviceIpAddress":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"sourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"destAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"destPort":"({dest_port}\d+)""""
  """"sourcePort":"({src_port}\d+)""""
  """"deviceName":"(({domain}[^\\\s\"]+)\\+)?({src_host}[^\\\s"]+)""""
  """"email":"(({domain}[^\\\s\"]+)\\+)?({user}[\w\.\-]{1,40}\$?)""""
  """"eventType":"({alert_name}[^"]+)""""
  """"threatIndicators":\[?\"({alert_type}[^\s\"]+)""""
  """"applicationPath":"({process_path}(({process_dir}[^\"=,]+?)[\\\/]+)?({process_name}[^\\\"\/]+))""""
  """"applicationName":"({process_name}[^"]+)""""
  """"targetPriorityType":"({alert_severity}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```