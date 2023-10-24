#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-notification-success-4654
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """EventID":4654""", """An IPsec Quick Mode negotiation failed""" ]
  Fields = [
  """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)"""
  """"EventID":({event_code}\d+)"""
  """({event_name}An IPsec Quick Mode negotiation failed)"""
  """"Computer":"({host}[\w\-.]+)"""
  """"TenantId":"({tenant_id}[^"]+)""""
  """"ManagementGroupName":"({group_name}[^"]+)""""
  """EventHub name:\s*({event_hub_name}[^\]]+?)\s*\]"""
  """"SourceSystem":"({app}[^"]+)""""
  """<Data Name\\?=\\?"RemoteAddress\\?">({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """<Data Name\\?=\\?"FailureReason\\?">({failure_reason}[^<]+)\s+?"""
  """<Data Name\\=\\?"LocalAddress\\?">({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """<Data Name\\=\\?"RemotePort\\?">({dest_port}\d+)"""
  """<Data Name\\=\\?"LocalPort\\?">({src_port}\d+)"""
  """({result}failed)"""
  ]
  ParserVersion = "v1.0.0"


}
```