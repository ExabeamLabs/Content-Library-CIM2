#### Parser Content
```Java
{
Name = extremenetworks-eciq-kv-endpoint-authentication-success-authsuccess
Vendor = Extreme Networks
Product = ExtremeCloud IQ
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """NETSIGHT:""", """Reason:""", """Device:""", """Switch:""" ]
Fields = [
   """Device\s*:\s*({dest_host}[^:]+?)(\s|,|$)""",
   """Switch\s*:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s|,|$)""",
   """Port\s*:\s*({src_port}\d+?)(\s|,|$)""",
   """MAC\s*:\s*({src_mac}[^:,]+?)(\s|,|$)""",
   """Reason\s*:\s*({event_name}[^:,]+?)(\s|,|$)""",
   """Severity\s+({severity}\S+?)(\s|,|$)"""
   ]
   ParserVersion = "v1.0.0"


}
```