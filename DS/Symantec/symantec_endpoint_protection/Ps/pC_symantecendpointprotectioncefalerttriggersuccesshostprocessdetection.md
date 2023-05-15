#### Parser Content
```Java
{
Name = symantec-endpointprotection-cef-alert-trigger-success-hostprocessdetection
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Symantec|ICDx|""", """"type":"HOST_PROCESS_DETECTION"""", """"product_name":"Symantec Integrated Cyber Defense Manager"""" ]
  Fields = [
  """"device_time":({time}\d{13})"""
  """\w{3,4} \d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)\s"""
  """dvchost=({src_host}[\w\-.]+)"""
  """suser=(none|SYSTEM|({user}[^\s]+))"""
  """dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """cs3Label=({alert_name}[^=]+?)\s*\w+="""
  """"type":"({alert_type}[^"]+)""""
  """"process":[^\}]+"path":"({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))""""
  """"uid":"({user_id}[^"]+)"""
  """Symantec\|([^=]+)\|({alert_severity}\w+)\|\w+="""
  """spt=({src_port}\d{1,5})"""
  """dpt=({dest_port}\d{1,5})"""
  """"device_domain":"({domain}[^"]+)""""
  """\sproto=({protocol}[^\s]+)\s"""
  """"md5":"({md5}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```