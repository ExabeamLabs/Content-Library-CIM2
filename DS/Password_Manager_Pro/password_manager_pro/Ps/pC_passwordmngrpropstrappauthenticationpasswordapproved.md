#### Parser Content
```Java
{
Name = passwordmngrpro-p-str-app-authentication-passwordapproved
  ParserVersion = v1.0.0
  Product = Password Manager Pro
  Conditions = [  """ Password_Approved """,""" Success """ ]
  Fields = ${PMPParsersTemplates.pmp-events.Fields} [
    """\sSuccess\s[^\s]+\s+({safe_value}[^:]+):(N\/A|({account}[^:\s]+))""",
  ]

pmp-events = {
  Vendor = Password Manager Pro
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """\s+(UserAudit:)?(System|N\/A|({user}({first_name}[^\s:_]+)(_({last_name}[^:\s]+))?)):(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+))\s+({event_name}Password_Retrieved|Password_Changed|Password_Approved|Password_Checked_In|Password_Checked_Out|Password_Requested|Personal_setting_changed|Resource_Exported|User_Authentication_Failed|User_Logged_in_-_SAML_Single_Sign_On|User_Logged_Out)""",
    """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """\w+ \d+ \d\d:\d\d:\d\d\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sSuccess\s[^\s]+\s+(?:-)?({user}({first_name}[^:_]+)(_({last_name}[^:]+))?):"""
  
}
```