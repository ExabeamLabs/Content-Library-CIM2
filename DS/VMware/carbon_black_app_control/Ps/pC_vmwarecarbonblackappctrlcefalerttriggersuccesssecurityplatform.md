#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-alert-trigger-success-securityplatform
Vendor = VMware
Product = Carbon Black App Control
TimeFormat = "MM dd yyyy HH:mm:ss"
Conditions = [
  """|Bit9|Security Platform|"""
  """ fname="""
]
Fields = [
  """({time}\d\d \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """(\||\s)dvc=(|({host}.+?))\s+(\w+=|$)"""
  """(\||\s)dvchost=(|({host}.+?))\s+(\w+=|$)"""
  """(\||\s)dst=(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(\w+=|$)"""
  """(\||\s)dhost=(|(\S+\\+)?({dest_host}.+?))\s+(\w+=|$)"""
  """(\||\s)duser=(|(({domain}NT AUTHORITY|[^\s\\]+)\\+)?({user}.+?))\s+(\w+=|$)"""
  """(\||\s)externalId=(|({alert_id}.+?))\s+(\w+=|$)"""
  """\|Bit9\|Security Platform\|(.*?\|){2}({alert_name}[^\|]+)\|"""
  """\|Bit9\|Security Platform\|(.*?\|){2}({access}[^\|]+)\|"""
  """\|Bit9\|Security Platform\|(.*?\|){2}({access}[^\|]+?)(\s*\([^|]+)?\|"""
  """\s<USER:({alert_severity}.+?)>\s"""
  """(\||\s)cat=(|({alert_type}.+?))\s+(\w+=|$)"""
  """(\||\s)deviceProcessName =(|({process_path}.+?))\s+(\w+=|$)"""
  """(\||\s)filePath=(|({file_path}(({file_dir}[^=]+[^\\])\\+)?({file_name}.+?)))\s+(\w+=|$)"""
  """(\||\s)fname=(|({file_name}.+?))\s+(\w+=|$)"""
  """(\||\s)fileHash=(|({old_hash}.+?))\s+(\w+=|$)"""
]
DupFields = [
  "old_hash->new_hash"
]
ParserVersion = "v1.0.0"


}
```