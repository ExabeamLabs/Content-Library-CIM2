#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-leef-peripheral-storage-tached
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
Conditions = [
  """LEEF:"""
  """|VMware_Carbon_Black|App_Control|"""
  """srcHostName ="""
  """policy="""
  """dstHostName ="""
  """tached|"""
]
Fields = [
  """devTime=({time}\w{1,3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d{1,3}\s\w{1,3})"""
  """\d\d:\d\d:\d\d\s({host}[^\s]+)\sLEEF"""
  """\|App_Control\|[^\|]+\|({operation}[^\|]+)"""
  """msg=Device\s+'({device_id}[^']+)'"""
  """msg=({operation_details}[^=]+?)\.\s"""
  """sev=({severity}\d+)"""
  """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """srcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[^\s]+)"""
  """usrName =(({domain}[^\\\s]+)\\+)?({user}[^\s]+)"""
  """dstHostName =({dest_host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```