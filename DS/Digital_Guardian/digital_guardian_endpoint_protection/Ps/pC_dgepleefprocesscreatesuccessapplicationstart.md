#### Parser Content
```Java
{
Name = dg-ep-leef-process-create-success-applicationstart
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """LEEF:""", """|Digital Guardian|Digital Guardian|""", """DigitalGuardian-Events""", """|Application Start|""" ]
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """accountName =(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\w+=|$)""",
    """IdentHostName =([^\\]+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """SourceDirectory=({process_dir}.+?)\s*(\w+=|$)""",
    """SourceFile=({process_name}.+?)\s*(\w+=|$)""",
  ]
  ParserVersion = v1.0.0


}
```