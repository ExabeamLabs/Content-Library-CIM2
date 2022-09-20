#### Parser Content
```Java
{
Name = microsoft-azure-kv-app-activity-changeuserlicense
  Conditions = [ """"category":"UserManagement"""", """"operationName":"Change user license"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}UserManagement)"""
  ]
  ParserVersion = "v1.0.0"

ms-azure-eventhubs-activity = {
  Vendor = Microsoft
  Product = Azure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"+callerIpAddress"+:"+(<null>|({src_ip}[A-Fa-f\d:.]+))"+""",
    """"+initiatedBy.*?"+userPrincipalName"+:"+({email_address}[^@]+@({email_domain}[^"]+))"+"""
    """"+targetResources.*?"+displayName"+:"+({object}[^"]+?)"+""",
    """"+targetResources.*?"+userPrincipalName"+:"+({object}[^"]+?)"+"""
    """"+targetResources.*?"+displayName"+:"+.*?\.DisplayName"+.*?"+newValue"+:[\"]*(null|({target}[^"\\]+))["\\]*"""
    """"+time"+:"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)"+"""
    """"+operationName"+:"+({operation}[^"]+)"+""",
    """"+result"+:"+({result}[^"]+)"+""",
    """({app}eventHubsAzureRecord)""",
    """({app}eventhubbeat_APL_Azure)""",
    """"app"+:\{[^\}]*?displayName"+:"+({app}[^",]+)"""",
    """object=({object}[^\|=\s]+)(\||\s\w+=)"""
  
}
```