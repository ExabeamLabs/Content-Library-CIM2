#### Parser Content
```Java
{
Name = zeek-z-json-http-session-zeekhttp
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "epoch_sec"
  Conditions = [ """ zeek_http """, """id.""" ]
  Fields = [
    """"ts"+:({time}\d{10})""",
    """"uid\\?"+:\\?"+({connection_id}[^"\\]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"trans_depth"+:({trans_depth}\d+)""",
    """({protocol}http)"""
  ]
  ParserVersion = "v1.0.0"


}
```