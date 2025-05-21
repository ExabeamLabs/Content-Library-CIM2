#### Parser Content
```Java
{
Name = microsoft-azuread-sk4-app-activity-success-other
  ParserVersion = "v1.0.0"
  Conditions = [ """"AuditLogs"""", """"Category":""", """"ProvisioningManagement"""", """"OperationName":""", """"Other"""" ]
  Fields = ${LMSMSParsersTemplates.cef-azure-audit.Fields} [
    """"ResultDescription":\s*"({additional_info}[^"]+)""",
    """({category}ProvisioningManagement)"""
  ]

cef-azure-audit {
     Vendor = Microsoft
     Product = Azure AD Activity Logs     
     TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
     Fields = [
       """"(TimeGenerated|time)":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(.\d{1,7})?Z)"""",
       """destinationServiceName =({app}Azure)""",
       """OperationName":\s*"({operation}[^"]+)""",
       """Category":\s*"({category}[^"]+)""",
       """CallerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
       """"Type":\s*"({event_category}[^"]+)""",
       """"type":\s*"({additional_info}[^"]+)""",
       """"Resource":\s*"({resource}[^"]+)""",
       """"ResourceId":\s*"({resource_id}[^",]+)""",
     ]
     DupFields = ["category->event_name", "resource->object"
}
```