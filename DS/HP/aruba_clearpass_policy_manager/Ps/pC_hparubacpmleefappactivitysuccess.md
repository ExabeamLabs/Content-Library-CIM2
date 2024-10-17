#### Parser Content
```Java
{
Name = hp-arubacpm-leef-app-activity-success
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """LEEF:""", """|Aruba Networks|ClearPass|""", """action=""", """entityName =""", """sub-cat=""", """usrName =""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+LEEF:""",
    """devTime=({time}[^=]+?)\s+\w+?=""",
    """action=(None|({operation}[^=]+?))\s+\w+?=""",
    """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """entityName =({object}[^=]+?)\s+""",
    """sub-cat=({object_type}[^=]+?)\s+\w+?=""",
    """usrName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+?=""",
    """({app}ClearPass)"""
   ]


}
```