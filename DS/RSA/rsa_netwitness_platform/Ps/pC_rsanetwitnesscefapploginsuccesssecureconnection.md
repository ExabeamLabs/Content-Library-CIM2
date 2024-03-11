#### Parser Content
```Java
{
Name = rsa-netwitness-cef-app-login-success-secureconnection
  Conditions = [ """CEF:""", """RSA|NetWitness Audit""", """Connection|SecureConnection""", """outcome=success""" ]
  ParserVersion = "v1.0.0"

cef-rsa-system-event = {
 Vendor = RSA
 Product = RSA NetWitness Platform
 TimeFormat = "MMM dd yyyy HH:mm:ss"
 Fields = [
   """rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)""",
   """src=(127.0.0.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
   """spt=({src_port}\d+)""",
   """sessionId=({session_id}\d+)""",
   """({app}NetWitness)""",
   """\Wsuser=((?i)system|({user}[^=\(]+))(\s\w+=|\()""",
   """outcome=({result}[^=]+?)\s\w+=""",
   """userRole=({role}[^=]+?)\s*(\w+=|$)""",
   """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)"""
   ]
 
}
```