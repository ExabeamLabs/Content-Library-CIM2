#### Parser Content
```Java
{
Name = microsoft-nps-csv-endpoint-login-success-ras
  Vendor = Microsoft
  Product = Microsoft Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","RAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","RAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("({domain}[^\\]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|[^,]*),("({src_host}[^,"\\\/]+)[^"]*?({full_name}[^"\\\/]+)"|[,]*),([^,]*,){8}("({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"|[^,]*),""",
    """(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w.\-]+))\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0


}
```