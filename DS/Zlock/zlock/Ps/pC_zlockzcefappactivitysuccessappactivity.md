#### Parser Content
```Java
{
Name = "zlock-z-cef-app-activity-success-appactivity"
Vendor = "Zlock"
Product = "Zlock"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Zlock|"""
]
Fields = [
  """({app}Zlock)"""
  """msg=({operation}.+?)\s+(\w+=|$)"""
  """suser=(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """shost=({src_host}[^\s]+)\s+(\w+=|$)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\srt=({time}\d{13})"""
  """sproc=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s+(\w+=|$)"""
  """fsize=({bytes}\d+)"""
  """cs2=({device_name}.+?)\s+(\w+=|$)"""
  """cs3=({policy_name}.+?)\s+(\w+=|$)"""
  """\sdvc=({host}\S+)(\s+\w+=|\s*$)"""
  """\sdvchost=({host}\S+)(\s+\w+=|\s*$)"""
  """fname=({file_path}({file_dir}[^=]*?[\\\/]+)?({file_name}[^\\\/=]+?(\.({file_ext}\w+))?))\s+\w+="""
]
DupFields = [
  "file_name->object"
]
ParserVersion = "v1.0.0"


}
```