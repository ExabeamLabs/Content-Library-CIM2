#### Parser Content
```Java
{
Name = "swivel-swivel-str-app-activity-success-pinsafe"
Vendor = "Swivel"
Product = "Swivel"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """ INFO """
  """ PINsafe["""
  """]: """
]
Fields = [
  """user[:\s]*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """({app}PINsafe)"""
  """\d\d:\d\d:\d\d\s({host}[a-fA-F\d.:]+)"""
  """INFO\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(-\s+)?({operation}.+?)\s*$"""
  """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s+({operation}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```