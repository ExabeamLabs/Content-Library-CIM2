#### Parser Content
```Java
{
Name = microsoft-azureatp-sk4-alert-trigger-success-deviceinfo
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure ATP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """CEF:""", """"category": "AdvancedHunting-DeviceInfo"""", """requestClientApplication=AzureATP""", """cat=audit""" ]
  Fields = [
  """"Timestamp":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,7}Z)"""
  """operationName":\s*"({action}[^"]+)"""
  """DeviceName":\s*"({host}[\w\-.]+)"""
  """"ClientVersion":"({client_version}[^"]+)""",
  """Sid\\":\\"({user_sid}[^"]+)\\""""
  """UserName\\":\\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\""""
  """"DomainName\\":\\"+({domain}[^"]+)\\"""",
  """"PublicIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"tenantId":\s"({tenant_id}[^",]+)""""
  """"DeviceCategory":"({device_category}[^"]+)""""
  """"DeviceId":"({device_id}[^"]+)""""
  ]
  DupFields = [ "host->dest_host" ]


}
```