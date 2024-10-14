#### Parser Content
```Java
{
Name = tufin-securetrack-kv-policy-modify-saved
 Product = Tufin SecureTrack
 Vendor = Tufin
 TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
 ParserVersion = "v1.0.0"
 Conditions = [ """ELM""", """Policy Saved:""", """revision ticket ids:"""]
 Fields =[
   """timestamp:\s+({time}\d+-\d+-\d+ \d+:\d+:\d+.\d+)""",
   """Policy (Saved|Fetched):\s+revision\s+(\d+)\s+on\s+({dest_host}[^\s;]+);""", #dl field removed
   """last modified by\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
   """ELM,.+?>({event_name}[^:]+:)\s+"""
   ]


}
```