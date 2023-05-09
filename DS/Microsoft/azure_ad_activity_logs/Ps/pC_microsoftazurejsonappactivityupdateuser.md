#### Parser Content
```Java
{
Name = microsoft-azure-json-app-activity-updateuser
  Conditions= [ """"category":"UserManagement"""", """"operationName":"Update user"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}UserManagement)"""
  ]
  ParserVersion = "v1.0.0"

ms-azure-eventhubs-activity = {
  Vendor = Microsoft
  Product = Azure AD Activity Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"+callerIpAddress"+:"+(<null>|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+""",
    """"+initiatedBy.*?"+userPrincipalName"+:"+({email_address}[^@]+@({email_domain}[^"]+))"+"""
    """"+targetResources.*?"+displayName"+:"+({object}[^"]+?)"+""",
    """"+targetResources.*?"+userPrincipalName"+:"+({object}[^"]+?)"+"""
    """"+targetResources.*?"+displayName"+:"+.*?\.DisplayName"+.*?"+newValue"+:[\\"]*(null|({target}[^"\\]+))["\\]"""
    """"+time"+:"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)"+"""
    """"+operationName"+:"+({operation}[^"]+)"+""",
    """"+result"+:"+({result}[^"]+)"+""",
    """({app}eventHubsAzureRecord)""",
    """({app}eventhubbeat_APL_Azure)""",
    """"app"+:\{[^\}]*?displayName"+:"+({app}[^",]+)"""",
    """object=({object}[^\|=\s]+)(\||\s\w+=)"""
  
}
```