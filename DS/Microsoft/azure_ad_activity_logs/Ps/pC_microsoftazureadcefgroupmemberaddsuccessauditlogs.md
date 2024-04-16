#### Parser Content
```Java
{
Name = "microsoft-azuread-cef-group-member-add-success-auditlogs"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""Resource":"Microsoft.aadiam""""
""""OperationName":"Add member to group""""
""""TenantId":""""
""""Type":"AuditLogs""""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)""",
""""userPrincipalName(\\)?":(\\)?"({email_address}[^"\\]+)"""
""""OperationName":"({operation}[^"]+)""""
""""Result":"({result}[^",]+)""""
""""Category":"({category}[^"]+)""""
""""app":\{[^,]+,"displayName":"({app}[^"]+)""""
""""LoggedByService":"(Core Directory|({app}[^"]+))"""",
"""({event_name}Add member to group)"""
"""Group\.DisplayName\\[^}]+"newValue\\":[\\"]+({group_name}[^"\\]+)"""
""""TargetResources":"\[\{\\"id\\":\\"({account_id}[^"\\]+)""",
""""displayName".*?Group\.ObjectID".*?newValue":"\\"?({group_id}[^\\"]+)\\"?""""
]
ParserVersion = "v1.0.0"


}
```