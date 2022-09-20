#### Parser Content
```Java
{
Name = rsa-netwitness-cef-app-logout-success-audit
  Conditions = [ """CEF:""", """RSA|NetWitness Audit""", """AUTHENTICATION|logoff""", """outcome=success""" ]
  ParserVersion = "v1.0.0"

cef-rsa-system-event = {
 Vendor = RSA
 Product = RSA NetWitness
 TimeFormat = "MMM dd yyyy HH:mm:ss"
 Fields = [
   """rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)""",
   """src=(127.0.0.1|({src_ip}[A-Fa-f.:\d]+))""",
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