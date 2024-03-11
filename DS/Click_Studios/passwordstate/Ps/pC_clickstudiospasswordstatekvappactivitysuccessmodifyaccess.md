#### Parser Content
```Java
{
Name = clickstudios-passwordstate-kv-app-activity-success-modifyaccess
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-mm-yyyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """granted Modify Access for""", """PasswordID =""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """Passwordstate:\s({full_name}[^\(]+?)\s\((({domain}[^\\\)\s]+)\\+)?({user}[^\)\s]+)\)""",
    """({event_name}granted Modify Access)"""
  ]
  ParserVersion = v1.0.0


}
```