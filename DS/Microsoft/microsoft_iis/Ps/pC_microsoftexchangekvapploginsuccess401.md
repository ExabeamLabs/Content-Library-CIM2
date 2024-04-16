#### Parser Content
```Java
{
Name = microsoft-exchange-kv-app-login-success-401
  Vendor = Microsoft
  Product = Microsoft IIS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """AgentDevice=MSIIS""", """sc-status=""" ]
  Fields = [
    """date=({time}\d\d\d\d\-\d\d\-\d\d\s*time\=\d\d:\d\d:\d\d)""",
    """SourceIp=({host}\S+)""",
    """s-ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """c-ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """cs-username=(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """cs\(User-Agent\)=({user_agent}.+?)\s*([\w\-\(\)]+=|$)""",
    """sc-bytes=({bytes_out}\d+)""",
    """cs-bytes=({bytes_in}\d+)""",
    """sc-status=(null|({http_response_code}\d+))\s*([\w\-\(\)]+=|$)""",
    """s-port=({protocol}.+?)\s*([\w\-\(\)]+=|$)""",
  ]


}
```