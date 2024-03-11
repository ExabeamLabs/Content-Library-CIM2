#### Parser Content
```Java
{
Name = microsoft-azure-mix-app-activity-success-caller
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"eventTimestamp":""", """"caller":""", """"resourceProviderName":""" ]
  Fields = ${MicrosoftAzureParsersTemplates.azure-app-activity-skyfromation.Fields} [
    """"resourceProviderName":\s*\{[^\}]*?"localizedValue":\s*"({resource}[^"]+)"""",
    """"eventTimestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """"operationName":\s*\{[^\}]*?"localizedValue":\s*"({operation}[^"]+)"""",
    """"resourceGroupName":"({user}[^"]+)"""",
    """"caller":\s*"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""",
    """"httpRequest":\s*\{[^\}]*?"clientIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\srequestClientApplication=({app}[^=]+)\s\w+=""",
    """"resourceId":"({object}[^"]+)""",
    """"resourceId":"[^"]*\/(?i)resourcegroups\/({account_id}[^\/"]+)\/"""
  ]


}
```