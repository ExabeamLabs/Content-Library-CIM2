#### Parser Content
```Java
{
Name = dg-ep-leef-file-upload-success-networktransferupload
  Product = Digital Guardian Endpoint Protection
  ParserVersion = v1.0.0
  Conditions = [ """LEEF:""", """|Digital Guardian|Digital Guardian|""", """DigitalGuardian-Events""", """|Network Transfer Upload|""" ]

leef-digitalguardian-file-operation = {
  Vendor = Digital Guardian
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """\|Digital Guardian\|([^\|]*\|){2}({event_code}[^\|]+)""",
    """accountName =(({domain}[^\\\s]+)\s*\\+)?({user}[^\\\s]+?)\s*(\w+=|$)""",
    """IdentHostName =([^\\]+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """Application=({app}.+?)\s*(\w+=|$)""",
    """srcBytes=({bytes}\d+)""",
    """DestinationDirectory=(|({file_dir}.+?))\s*(\w+=|$)""",
    """DestinationFile=(|({file_name}.+?(\.({file_ext}[^\.]+?))?))\s*(\w+=|$)""",
    """SourceDirectory=(|({src_file_dir}.+?))\s*(\w+=|$)""",
    """SourceFile=(|({src_file_name}.+?))\s*(\w+=|$)""",
  
}
```