#### Parser Content
```Java
{
Name = salesforce-sf-kv-app-login-logingeoid
  Vendor =  Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LoginGeoId=""","""|Quicklook_ID__c=""" ]
  Fields = [
    """\|Name ="({user}[^"]+)"""",
    """\|LoginTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|SourceIp="({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\|LoginUrl="({src_host}[^"]+)"""",
    """\|Browser="(Unknown|({browser}[^"]+))"""",
    """\|Platform="(Unknown|({os}[^"]+))"""",
    """\|Status="({result}[^"]+)"""",
    """\|Application="({app}[^"]+)"""",
  ]
  DupFields = [ "result->failure_reason" ]
  ParserVersion = v1.0.0


}
```