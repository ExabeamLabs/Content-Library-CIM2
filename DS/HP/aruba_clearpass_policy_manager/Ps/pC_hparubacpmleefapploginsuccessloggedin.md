#### Parser Content
```Java
{
Name = hp-arubacpm-leef-app-login-success-loggedin
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """LEEF:""", """|Aruba Networks|ClearPass|""", """sub-cat=Logged in""", """cat=System Events""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+LEEF:""",
    """devTime=({time}[^=]+?)\s+\w+?=""",
    """action=(None|({operation}[^=]+?))\s+\w+?=""",
    """src=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+\w+?="""
    """sub-cat=({event_name}[^=]+?)\s+\w+?=""",
    """Client IP Address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User:\s*({user}[^\s\\]+)""",
    """({app}ClearPass)"""
  ]
  DupFields = [ "event_name->operation" ]
  ParserVersion = "v1.0.0"


}
```