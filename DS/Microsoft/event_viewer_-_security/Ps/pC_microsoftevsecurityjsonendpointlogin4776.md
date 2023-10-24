#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4776"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
    """4776"""
    """"PackageName":""""
    """attempted to validate the credentials for an account"""
  ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)""""
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
    """"EventTime":({time}\d+)"""
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"(Hostname|MachineName)":"({host}[^"]*)"""
    """"Computer"+:"+({host}[\w\-.]+)""""
    """"Computer"+:"+({dest_host}[\w\-.]+)""""
    """({event_code}4776)"""
    """"TargetUserName":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?))"""   
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
    """"(Hostname|MachineName)":"(?!(?:[A-Fa-f:\d.]+))[^."]*\.({domain}[^.]*)"""
    """"TargetUserName":"[^"@]+(?:@({domain}[^"@\s]+)[^"]*)?"""
    """"Status":"({result_code}[^"]*)"""
    """"Workstation":"\\*({src_host}[^"]+)"""
    """Logon Account:((\\)[rnt])*({account}.+?)((\\)[rnt])*Source Workstation"""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```