#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-user-password-modify-success
  Conditions = [ """LEEF:""", """|BeyondTrust|BeyondInsight|""", """EventDesc=Password change is successful""", """cat=Change""" ]
  ParserVersion = "v1.0.0"

leef-beyondtrust-beyondinsight = {
   Vendor = BeyondTrust
   Product = BeyondInsight
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Fields = [
    """cat=({event_name}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """EventDesc=({event_name}[^=]+?)(\\t|\\r|\\s|\\)\w+=""",
    """devTime=({time}\w{3}\s+\d\d\s+\d\d\d\d\s+\d\d:\d\d:\d\d)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """EventName =({category}[^=]+?)(\\t|\\r|\\n|\\s|=)""",
    """HostName =({host}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """UserName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\\s)*\w+=""",
    """Message=({additional_info}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """Result=({result}[^=]+?)(\\t|\\r|\\n|\\s)*\w+="""
   ]
 
}
```