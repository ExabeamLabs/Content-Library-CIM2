#### Parser Content
```Java
{
Name = microsoft-o365-mix-app-login-success-teamssessionstarted
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Workload""", """"Operation":"TeamsSessionStarted"""" ]
  Fields = [
    """"CreationTime":"({time}\d+\-\d+\-\d+T\d+:\d+:\d+)"""",
    """"Workload":"({app}[^"]+)"""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """sourceDnsDomain=({domain}[^=]+?)\s+\w+=""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^\s"]+))?)""",
    """"Operation":"({operation}[^"]+)"""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"ObjectId":"(Unknown \(Unknown\)|({os}[A-Za-z]+[^"]*))\s*""""
    """"UserType":"*({user_type}[^,}"]+)"*"""
  ]


}
```