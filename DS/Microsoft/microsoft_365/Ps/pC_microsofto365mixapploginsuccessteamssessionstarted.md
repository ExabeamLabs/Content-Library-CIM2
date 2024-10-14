#### Parser Content
```Java
{
Name = microsoft-o365-mix-app-login-success-teamssessionstarted
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Workload""", """"Operation":""",""""TeamsSessionStarted"""" ]
  Fields = [
    """"CreationTime":"({time}\d+\-\d+\-\d+T\d+:\d+:\d+)"""",
    """"Workload":"({app}[^"]+)"""",
    """"+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """UserId"*:\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"*"""
    """sourceDnsDomain=({domain}[^=]+?)\s+\w+=""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s"]+))?)""",
    """"Operation":"({operation}[^"]+)"""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"UserType":"*({user_type}[^,}"]+)"*"""
    """exa_json_path=$.CreationTime,exa_field_name=time"""
    """exa_json_path=$.Workload,exa_field_name=app"""
    """exa_json_path=$.Operation,exa_field_name=operation"""
    """exa_json_path=$.UserType,exa_field_name=user_type"""
    """exa_regex=ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex=UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+""",
    """exa_regex=UserId"*:\s*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"*"""
    """ObjectId"*:\s*"*((?i)(Unknown)|({object}[^"]+))"*"""
    """exa_regex=ObjectId"*:\s*"*((?i)(Unknown)|({object}[^"]+))"*"""
  ]


}
```