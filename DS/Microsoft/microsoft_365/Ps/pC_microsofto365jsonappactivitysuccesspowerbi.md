#### Parser Content
```Java
{
Name = "microsoft-o365-json-app-activity-success-powerbi"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """Workload"""
  """PowerBI"""
  """WorkspaceId"""
]
Fields = [
  """"*CreationTime"*:\s*"*({time}\d+-\d+-\d+T\d+:\d+:\d+)"*"""
  """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s+[\w\-.]+\s+"""
  """destinationServiceName =({app}.*?)\s*deviceInboundInterface"""
  """Workload"*:\s*"*({app}[^"]+)"*"""
  """"ObjectId"*:\s*"*(null|({object}[^"]+))"*""",
  """"Operation"*:\s*"*({operation}[^"]+)"*""",
  """UserId"*:\s*"*({email_address}[^@]+@({email_domain}[^"]+))"*"""
  """"userPrincipalName":"({email_address}[^"@\s]+@({email_domain}[^"@\s]+))""""
  """"ipAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"ClientIP"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """UserAgent"*:\s*"*({user_agent}[^"]+)"*,"""
  """DatasetName"*:\s*"*({data_set_name}[^"]+)"""
  """Workload"*:\s*"*({resource}[^"]+)"*"""
  """"IsSuccess":\s*({result}[\w]+)"""
]
ParserVersion = "v1.0.0"


}
```