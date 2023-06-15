#### Parser Content
```Java
{
Name = dg-ep-leef-file-read-success-fileopen
  Product = Digital Guardian Endpoint Protection
  ParserVersion = v1.0.0
  Conditions = [ """LEEF:""", """|Digital Guardian|Digital Guardian|""", """DigitalGuardian-Events""", """|File Open|""" ]

leef-digitalguardian-file-operation = {
  Vendor = Digital Guardian
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """\|Digital Guardian\|([^\|]*\|){2}({event_code}[^\|]+)""",
    """accountName =(({domain}[^\\\s]+)\s*\\+)?({user}[^\\\s]+?)\s*(\w+=|$)""",
    """IdentHostName =([^\\]+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Application=({app}.+?)\s*(\w+=|$)""",
    """srcBytes=({bytes}\d+)""",
    """DestinationDirectory=(|({file_dir}.+?))\s*(\w+=|$)""",
    """DestinationFile=(|({file_name}.+?(\.({file_ext}[^\.]+?))?))\s*(\w+=|$)""",
    """SourceDirectory=(|({src_file_dir}.+?))\s*(\w+=|$)""",
    """SourceFile=(|({src_file_name}.+?))\s*(\w+=|$)""",
  
}
```