#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-login-success-61025
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Conditions = [ """CISE""", """61025""", """Open secure connection with TLS peer""" ] 
  Fields = [
  """({event_code}61025)\s+({alert_severity}[^\s]+)\s({operation}[^:]+):\s+({event_name}[^,]+)"""
  """\d\d:\d\d:\d\d\s({host}[^\s]+) CISE_"""
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d (-|\+)\d\d:\d\d)"""
  """(?:client IP|AdminIPAddress)(?::|=)\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """OperationMessageText=({additional_info}[^,]+)"""
  """AdminInterface=(UNKNOWN|({admin_interface}[^,]+))"""  
  """\s*ConfigVersionId=({badge_id}\d+)"""
  ]


}
```