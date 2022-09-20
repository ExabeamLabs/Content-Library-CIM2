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
    """accountName =(({domain}[^\\]+)\\+)?({user}[^\\\s]+?)\s*(\w+=|$)""",
    """IdentHostName =([^\\]+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """SourceDirectory=({process_dir}.+?)\s*(\w+=|$)""",
    """SourceFile=({process_name}.+?)\s*(\w+=|$)""",
  ]
  ParserVersion = v1.0.0


}
```