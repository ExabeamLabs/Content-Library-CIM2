#### Parser Content
```Java
{
Name = dg-ep-leef-endpoint-login-success-23
  Conditions = [ """LEEF:""", """|Digital Guardian|Digital Guardian|""", """DigitalGuardian-Events""", """|23|""" ]
  ParserVersion = v1.0.0

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