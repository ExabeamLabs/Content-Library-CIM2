#### Parser Content
```Java
{
Name = "microsoft-azure-cef-file-write-success-secretset"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ResourceId":"""
  """OperationName":"SecretSet"""
]
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""
  """"ResourceProvider\":\"({object}[^\"]+)"""
  """"ResourceId\":\"({file_path}({file_dir}(?:[^\";]+)?[\/;])?({file_name}[^\/\";]+))\""""
  """"Resource\":\"({file_name}[^\"]+?(\.({file_ext}[^\s\."]+))?)\""""
  """suser=((?i)anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """devicePayloadId=.+\s+name\s+:\s+\[({host}[^\]]+)"""
  """fileType=({file_type}[^\s]+)"""
  """"CallerIPAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
  """"ResultType\":\"({result}[^\"]+)"""
  """requestClientApplication=({app}.+?)\s\w+="""
  """"OperationName\":\"({event_name}[^\"]+)\""""
  """({access}resource-created)"""
  """msg=({additional_info}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```