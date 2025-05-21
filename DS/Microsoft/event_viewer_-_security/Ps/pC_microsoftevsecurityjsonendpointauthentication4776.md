#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-authentication-4776
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4776""", """"Category":"Credential Validation"""", """Microsoft-Windows-Security-Auditing""", """"Channel":"Security"""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[\w\-.]+)"""",
    """"EventID":({event_code}\d+)""",
    """"Workstation":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(?:(?!NULL)(\\*({src_host}[^\s"]+))))"""",
    """"TargetUserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s"@]+))?)"""",
    """"Status":"({result_code}[^"]+)"""",
    """"RecordNumber":({event_id}\d+),""",
    """"Severity":"({severity}[^"]+)"""",
    """"SourceName":"({provider_name}[^"]+)"""",
    """"Category":"({event_name}[^"]+)"""",
    """"PackageName":"({auth_package}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```