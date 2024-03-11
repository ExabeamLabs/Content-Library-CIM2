#### Parser Content
```Java
{
Name = dg-ep-leef-peripheral-storage-insert-success-44
Vendor = "Digital Guardian"
Product = "Digital Guardian Endpoint Protection"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """LEEF:"""
  """|Digital Guardian|Digital Guardian|"""
  """DigitalGuardian-Events"""
  """|44|"""
]
Fields = [
  """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """({host}[\w\-.]+) LEEF:"""
  """\|Digital Guardian\|([^\|]*\|){2}({event_code}[^\|]+)"""
  """accountName =(({domain}[^\\\s]+)\s*\\+)?({user}[^\\\s]+?)\s*(\w+=|$)"""
  """IdentHostName =([^\\]+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)"""
  """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """DestinationFile=(|({file_name}.+?(\.({file_ext}[^\.]+?))?))\s*(\w+=|$)"""
  """SourceDriveType=(|({device_type}.+?))\s*(\w+=|$)"""
  """SourceDeviceID=(|({device_id}.+?))\s*(\w+=|$)"""
  """SourceDeviceFriendlyName =(|({operation_details}.+?))\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```