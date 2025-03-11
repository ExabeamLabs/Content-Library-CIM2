#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-password-read-success-5382
   Product = Event Viewer - Security
   Vendor = Microsoft
   ParserVersion = v1.0.0
   TimeFormat = "MM/dd/yyyy hh:mm:ss a"
   Conditions = [ """EventCode=5382""", """Microsoft Windows security auditing""", """Vault credentials were read""" ]
   Fields =[
     """ComputerName =({host}[\w\-\.]+)"""
     """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))\sLogName ="""
     """Keywords=({result}[^=]+?)\s\w+="""
     """TaskCategory=({task}[^=]+?)\s*\w+="""
     """({event_name}Vault credentials were read)"""
     """Subject:\s*Security ID:\s*({user_sid}[^:]+?)\s*Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}[^:]+?)\s*Logon ID:\s*({login_id}[^:]+?)\s"""
     ]
   

}
```