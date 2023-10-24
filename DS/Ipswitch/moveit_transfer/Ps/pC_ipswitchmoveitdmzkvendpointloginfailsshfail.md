#### Parser Content
```Java
{
Name = ipswitch-moveitdmz-kv-endpoint-login-fail-sshfail
  ParserVersion = v1.0.0
  Conditions = [ """AgentBrand: MOVEit""", """FAILED: SSH"""]
  Fields = ${MoveITParsersTemplates.moveit-activity.Fields} [
     """\sMessage:\s*({failure_reason}[^,\.]+)""",
  ]

moveit-activity = {
  Vendor = Ipswitch
  Product = MoveIt Transfer
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
    """\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """User\s'(({email_address}[^@]+@[^']+)|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-]{1,40}\$?)?\)"""
    """\s:\s+({operation}[^,]+),\s+ID:"""
    """\sUsername:\s*(Automation|({user}[\w\.\-]{1,40}\$?))"""
   
}
```