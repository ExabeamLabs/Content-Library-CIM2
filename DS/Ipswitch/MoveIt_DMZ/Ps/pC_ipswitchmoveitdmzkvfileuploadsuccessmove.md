#### Parser Content
```Java
{
Name = ipswitch-moveitdmz-kv-file-upload-success-move
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Move"""]
  Fields = ${MoveITParsersTemplates.moveit-activity.Fields} [
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({src_file_name}[^,]+)"""
    """\sFolderPath:\s*({src_file_path}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
    """({operation}Move)"""
    """IPAddress:\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""

  ]
  DupFields = [ "src_file_name->file_name" ]

moveit-activity = {
  Vendor = Ipswitch
  Product = MoveIt DMZ
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
    """\sIPAddress:\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
    """User\s'(({email_address}[^@]+@[^']+)|Automation|({full_name}[^']+))?'\s\(({user}[^\)]+)?\)"""
    """\s:\s+({operation}[^,]+),\s+ID:"""
    """\sUsername:\s*(Automation|({user}[^,]+))"""
   
}
```