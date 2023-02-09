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
    """\|SourceIp="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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