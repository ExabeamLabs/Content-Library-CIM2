#### Parser Content
```Java
{
Name = clickstudios-passwordstate-kv-user-password-reset-success-resetsuccess
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-mm-yyyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """The Passwordstate Windows Service successfully reset the password for""", """PasswordID =""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """({event_name}The Passwordstate Windows Service successfully reset the password)"""
  ]
  ParserVersion = v1.0.0


}
```