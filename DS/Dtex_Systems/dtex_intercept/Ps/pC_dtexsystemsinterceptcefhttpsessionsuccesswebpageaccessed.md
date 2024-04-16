#### Parser Content
```Java
{
Name = dtexsystems-intercept-cef-http-session-success-webpageaccessed
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Dtex|""", """|NetworkActivity|WebPageAccessed|""" ]
  Fields = [
    """\Wstart=({time}\d{13})""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """"OsPlatform":\s*"({os}[^"]+)""",
    """"ContentType":\s*"({mime}[^"]+)""",
    """"Referrer":\s*"({referrer}[^"]+)""",
    """Network_Remote_Port=({dest_port}\d+)""",
    """Website_Protocol=({protocol}[^\s"]+)""",
    """Website_Query=({url}[^\s"]+)""",
    """Website_Query=(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)""",
    """Website_Query=(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))""",
    """Website_Query=(?:[^:]+:\/+)({web_domain}[^\/:\s]+)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s""",
    """([^\|]*\|){5}({action}[^\|]+)""",
  ]
  DupFields = [ "host->src_host" ]
  ParserVersion = "v1.0.0"


}
```