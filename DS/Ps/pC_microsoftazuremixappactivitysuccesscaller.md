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
    """\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"caller":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"resourceGroupName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"caller":\s*"((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"httpRequest":\s*\{[^\}]*?"clientIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\srequestClientApplication=({app}[^=]+)\s\w+=""",
    """"resourceId":"({object}[^"]+)""",
    """"resourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """"resourceId":"[^"]*\/(?i)resourcegroups\/({account_id}[^\/"]+)\/"""
    """"operationName":\s*\{[^\}]*?"localizedValue":\s*"({db_operation}[^"]+)"""",
    """request=({result}[^=\s]+)\s+\w+=""",
    """sourceServiceName =\s*({service_name}[^=]+)\s+\w+=""",
    """"category":\s*\{[^\}]*?"localizedValue":\s*"({category}[^"]+)""""
    """"Description_scrubbed":"({additional_info}[^=",]+)""""
    """"resourceId":"[^"]+?\/DATABASES\/({db_name}[^\/"]+)""""
    """exa_json_path=$.resourceProviderName.localizedValue,exa_field_name=resource"""
    """exa_json_path=$.caller,exa_regex=((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.httpRequest.clientIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  ]


}
```