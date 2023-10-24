#### Parser Content
```Java
{
Name = "imanage-i-kv-app-activity-success-appactivity"
Vendor = "iManage"
Product = "iManage"
TimeFormat = "dd/MM/yyyy HH:mm:ss"
Conditions = [
  """ ACTIVITY = """
  """ ACTIVITY_DATETIME = """
  """ DOCNUM = """
]
Fields = [
  """ACTIVITY_DATETIME\s*=\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)"""
  """DOCNUM\s*=\s*({object}.+?)\s+(\w+\s+=|$)"""
  """ACTIVITY\s*=\s*({operation}.+?)\s+(\w+\s+=|$)"""
  """DOCUSER\s*=\s*({user}[\w\.\-]{1,40}\$?)\s+(\w+\s+=|$)"""
  """APPNAME\s*=\s*({additional_info}.+?)\s+(\w+\s+=|$)"""
  """LOCATION\s*=\s*({dest_host}[\w\-.]+)\s+(\w+\s+=|$)"""
  """DOCNAME\s*=\s*({resource}.+?)\s+(\w+\s+=|$)"""
  """DOCLOC\s*=\s*({file_path}({file_dir}.+?)[\\\/]*({file_name}[^\\\/]+?))\s+(\w+\s+=|$)"""
]
ParserVersion = "v1.0.0"


}
```