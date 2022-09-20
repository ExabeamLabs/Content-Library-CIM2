#### Parser Content
```Java
{
Name = microsoft-nps-csv-endpoint-login-success-ias
  Vendor = Microsoft
  Product = Network Policy Server
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("host\/({src_host}[^,"]+?)"|[,]*),("({domain}[^\\]+)\\+({user}[^"]+)"|[^,]*),([^,]*,){8}("({src_ip}[a-fA-F\d.:]+)"|[^,]*),""",
    """({dest_host}[\w.\-]+)\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0


}
```