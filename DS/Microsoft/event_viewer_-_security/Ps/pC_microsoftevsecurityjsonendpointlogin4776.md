#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4776"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
    """4776"""
    """"PackageName":""""
    """attempted to validate the credentials for an account"""
  ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)""""
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
    """"EventTime":({time}\d+)"""
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"(Hostname|MachineName)":"({host}[^"]*)"""
    """"Computer"+:"+({host}[\w\-.]+)""""
    """"Computer"+:"+({host}[\w\-.]+)""""
    """({event_code}4776)"""
    """"TargetUserName":"(({user_upn}[^@"]+@[^\."]+(\.[^"]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""   
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
    """"(Hostname|MachineName)":"(?!(?:[A-Fa-f:\d.]+))[^."]*\.({domain}[^.]*)"""
    """"TargetUserName":"[^"@]+(?:@({domain}[^"@\s]+)[^"]*)?"""
    """"Status":"({result_code}[^"]*)"""
    """"Workstation":"\\*({src_host}[^"]+)"""
    """Logon Account:((?-i)\\+[rnt])*({account}.+?)((?-i)\\+[rnt])*Source Workstation"""
    """"eventRecordID":"({event_id}\d+)""""
    """"severityValue":"({result}[^"]+?)\s*""""
  ]
  DupFields = [ "result_code->failure_code", "domain->dest_domain", "user->dest_user" ]


}
```