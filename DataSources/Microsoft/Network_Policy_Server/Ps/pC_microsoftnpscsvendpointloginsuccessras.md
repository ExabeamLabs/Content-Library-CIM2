#### Parser Content
```Java
{
Name = microsoft-nps-csv-endpoint-login-success-ras
  Vendor = Microsoft
  Product = Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","RAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","RAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("({domain}[^\\]+)\\+({user}[^"]+)"|[^,]*),("({src_host}[^,"\\\/]+)[^"]*?({full_name}[^"\\\/]+)"|[,]*),([^,]*,){8}("({src_ip}[a-fA-F\d.:]+)"|[^,]*),""",
    """({dest_host}[\w.\-]+)\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0


}
```