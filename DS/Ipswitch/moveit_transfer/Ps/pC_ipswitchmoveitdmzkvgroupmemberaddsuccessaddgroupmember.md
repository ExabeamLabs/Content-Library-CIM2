#### Parser Content
```Java
{
Name = ipswitch-moveitdmz-kv-group-member-add-success-addgroupmember
  Conditions = [ """MOVEitDMZ""", """Add Group Member"""]
  Fields = ${MoveITParsersTemplates.moveit-activity.Fields} [
     """TargetName:\s+({dest_user}[^,]+)""",
     """TargetID:\s+({dest_user_sid}[^,]+)""",
     """({operation}Add Group Member)""",
     """\sID:\s({account_id}\d+)""",
  ]
  ParserVersion = "v1.0.0"

moveit-activity = {
  Vendor = Ipswitch
  Product = MoveIt Transfer
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
    """\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """User\s'(({email_address}[^@]+@[^']+)|Automation|({full_name}[^']+))?'\s\(({user}[^\)]+)?\)"""
    """\s:\s+({operation}[^,]+),\s+ID:"""
    """\sUsername:\s*(Automation|({user}[^,]+))"""
   
}
```