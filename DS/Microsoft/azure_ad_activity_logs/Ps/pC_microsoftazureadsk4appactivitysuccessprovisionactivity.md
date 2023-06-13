#### Parser Content
```Java
{
Name = microsoft-azuread-sk4-app-activity-success-provisionactivity
  ParserVersion = "v1.0.0"
  Conditions = ["""CEF:""", """destinationServiceName =Azure""", """"Type":"AADProvisioningLogs"""", """"OperationName":"Provisioning activity"""" ]
  Fields = ${LMSMSParsersTemplates.cef-azure-audit.Fields} [
    """"ResultDescription":"({additional_info}[^"]+)""",
  ]

cef-azure-audit {
     Vendor = Microsoft
     Product = Azure AD Activity Logs     
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
     Fields = [
       """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
       """destinationServiceName =({app}Azure)""",
       """OperationName":"({operation}[^"]+)""",
       """Category":"({category}[^"]+)""",
       """CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
       """"Type":"({event_category}[^"]+)""",
       """"type":"({additional_info}[^"]+)""",
       """"Resource":"({resource}[^"]+)""",
       """"ResourceId":"({resource_id}[^",]+)""",
     ]
     DupFields = ["category->event_name", "resource->object"
}
```