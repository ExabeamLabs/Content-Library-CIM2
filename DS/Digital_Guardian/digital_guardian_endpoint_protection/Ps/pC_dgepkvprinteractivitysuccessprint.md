#### Parser Content
```Java
{
Name = dg-ep-kv-printer-activity-success-print
Conditions = [
  """Operation="Print""""
  """Agent_UTC_Time="""
]
ParserVersion = "v1.0.0"

leef-digitalguardian-local-logon = {
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """accountName =(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)""",
    """IdentHostName =([^\\]+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """Application=({process_name}.+?)\s*(\w+=|$)""",
    """({event_code}User Logon)""",
  
}
```