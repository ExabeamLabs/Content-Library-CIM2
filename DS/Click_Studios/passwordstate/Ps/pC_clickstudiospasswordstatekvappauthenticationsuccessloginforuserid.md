#### Parser Content
```Java
{
Name = clickstudios-passwordstate-kv-app-authentication-success-loginforuserid
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-mm-yyyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """Successful""", """login for UserID"""]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Passwordstate:\s+({result}Successful)\s""",
    """({event_name}Successful 'SAML' login for UserID)""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """UserID\s+'(({domain}[^']+)\\)?({user}[^']+)"""
  ]
  ParserVersion = v1.0.0


}
```