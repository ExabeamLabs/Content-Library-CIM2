#### Parser Content
```Java
{
Name = rsa-ram-str-user-lock-success-idlockedout
  Conditions = [ """AAOP-Audit""", """USER_ID_LOCKED_OUT""" ]
  ParserVersion = "v1.0.0"

rsa-account-activity = {
  Vendor = RSA
  Product = RSA Adaptive Authentication
  TimeFormat = "yyyy-MM-dd HH:mm:ss,SSS Z"
  Fields = [
    """\s({host}[^\s]+)\s+AAOP-Audit""",
    """\s({host}[^\s]+)\s+AAOP-Audit\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(,\d+ (\+|-)\d+)?)\s+\|[^\|]+\|\s[^\s]+\s\|\s*\[?({user_id}[^\]\|\s]+)\s+\|\s*([^\s\|]+)\s+\|\s*((?i)DEVID_UNDEFINED|({device_id}[^\s\|]+))\s+\|\s((?i)IP_UNDEFINED|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\|\s*([^\|]+)\s+\|\s*({event_name}[^\|]+)\s+\|\s*((?i)EVENTID_UNDEFINED|({event_code}[^\|]+))\s+\|\s*((?i)TRANSID_UNDEFINED|({transaction_id}[^\|]+))\s+\|\s*((?i)TRANSTYPE_UNDEFINED|({result}[^\|]+))\s+\|\s*""", #dl field removed
  ]
 }

 cef-rsa-system-event = {
 Vendor = RSA
 Product = RSA NetWitness Platform
 TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
 Fields = [
   """rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)""",
   """src=(127.0.0.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
   """spt=({src_port}\d+)""",
   """sessionId=({session_id}\d+)""",
   """({app}NetWitness)""",
   """\Wsuser=((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s\w+=|\()""",
   """outcome=({result}[^=]+?)\s\w+=""",
   """userRole=({role}[^=]+?)\s*(\w+=|$)""",
   """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)"""
   ]
 
}
```