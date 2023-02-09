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
   """Switch\s*:\s*({src_ip}[A-Fa-f\d.:]+?)(\s|,|$)""",
   """Port\s*:\s*({src_port}\d+?)(\s|,|$)""",
   """MAC\s*:\s*({src_mac}[^:,]+?)(\s|,|$)""",
   """Reason\s*:\s*({event_name}[^:,]+?)(\s|,|$)""",
   """Severity\s+({severity}\S+?)(\s|,|$)"""
   ]
   ParserVersion = "v1.0.0"


}
```