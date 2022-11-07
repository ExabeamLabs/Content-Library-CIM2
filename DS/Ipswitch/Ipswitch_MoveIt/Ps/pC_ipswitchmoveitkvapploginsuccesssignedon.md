#### Parser Content
```Java
{
Name = ipswitch-moveit-kv-app-login-success-signedon
  ParserVersion = "v1.0.0"
  Product = Ipswitch MoveIt
  Conditions = [ """AgentBrand: MOVEit""", """Signed on"""]
  Fields = ${MoveITParsersTemplates.moveit-activity.Fields} [
     """\sMessage:\s*({additional_info}[^,\.]+)""",
  ]

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