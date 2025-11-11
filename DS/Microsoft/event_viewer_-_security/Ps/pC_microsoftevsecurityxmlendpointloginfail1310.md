#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-login-fail-1310
 ParserVersion = v1.0.0
 Vendor = Microsoft
 Product = Event Viewer - Security
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
 Conditions = [ """<EventID Qualifiers""","""'16640'>1310<""", """Failed NTLM Authentication"""]
 Fields = [
   """<Provider Name\\*='({provider_name}[^']+)""",
   """<EventID Qualifiers\\*='16640'>({event_code}[^<]+)""",
   """<Keywords>({result}[^<]+)""",
   """<TimeCreated SystemTime\\*=('|")({time}.+?)('|")""",
   """<EventRecordID>({event_id}[^<]+)""",
   """<Computer>({dest_host}({host}[\w\-.]+))""",
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
   """status=([^:]+:)({failure_code}({result_code}[^:]+)):"""
   """Failed NTLM Authentication for user:\s+'({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
   """<Message>({event_name}.+?)\s{0,100}<"""
   """status=([^:]+:){2}({failure_reason}.+?)\s<"""
   """<Level>({run_level}[^<]+)<"""
   ]


}
```