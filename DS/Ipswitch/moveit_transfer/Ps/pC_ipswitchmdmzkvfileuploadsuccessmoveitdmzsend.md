#### Parser Content
```Java
{
Name = "ipswitch-mdmz-kv-file-upload-success-moveitdmzsend"
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Send""" ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
  """\sFileID:\s*({file_id}[^,]+)"""
  """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
  """\sFolderPath:\s*({file_path}[^,]+)"""
  """\sXFerSize:\s*({bytes}\d+)"""
  """({operation}Send)"""
  """TargetName:\s({full_name}[^,]+)"""
  """Parm2:\s({email_address}[^@]+@[^\.]+\.[^,]+)"""
  ]

moveit-activity = {
  Vendor = Ipswitch
  Product = MoveIt Transfer
  TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
    """\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-]{1,40}\$?)?\)"""
    """\s:\s+({operation}[^,]+),\s+ID:"""
    """\sUsername:\s*(Automation|({user}[\w\.\-]{1,40}\$?))"""
   
}
```