#### Parser Content
```Java
{
Name = microsoft-azure-json-role-write-success-createroledefination
  Vendor = Microsoft
  Product = Microsoft Azure
  ParserVersion = v1.0.0
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  Conditions = [ """localizedValue":"Create or update custom role definition""" ]
  Fields = ${MSParserTemplates.azure-activity-json.Fields} [
    """"+requestbody"+:[^\}]+"+roleName\\?"+:\s*\\?"+({role}[^"]+)\\"+""",
    """"+requestbody"+:[^\}]+"+description\\?"+:\s*\\?"+({additional_info}[^"]+)\\"+""",
    """"+requestbody"+:[^\}]+"+assignableScopes\\?"+:\s*\[({assignble_scope}[^\]\[]+)\]""",
    """"+requestbody"+:[^\}]+"+permissions\\?"+:\s*\[({role_definition}\{[^;]+\})\]""",
    """"+requestbody"+:[^\}]+"+actions\\?"+:\s*\[({allowed_permissions}[^\]]+)\]""",
    """"+requestbody"+:[^\}]+"+dataActions\\?"+:\s*\[({allowed_data_actions}[^\]]+)\]""",
    """"+requestbody"+:[^\}]+"+notDataActions\\?"+:\s*\[({denied_data_actions}[^\]]+)\]""",
  ]

azure-activity-json = {
    Vendor = Microsoft
    Product = Microsoft Azure
    TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
    Fields = [
      """"+eventTimestamp"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+""",
      """"+authorization"+:[^\}]+scope"+:\s*"+({authorization_scope}[^"]+)""", 
      """"+caller"+:\s*"+({email_address}[^"]+@({email_domain}[^"]+))""",
      """"+claims"+:[^\}]+ipaddr"+:\s*"+({src_ip}[^"]+)"+""",
      """"+correlationId"+:\s*"+({correlation_id}[^"]+)""",
      """"+eventName"+:[^\}]+value"+:\s*"+({operation_first}BeginRequest)"+""",
      """"+eventName"+:[^\}]+value"+:\s*"+({operation_last}EndRequest)"+""",
      """"+category"+:[^\}]+value"+:\s*"+({event_category}[^"]+)"+""",
      """"+operationName"+:[^\}]+value"+:\s*"+({operation}[^"]+)"+""",
      """"+operationName"+:[^\}]+localizedValue"+:\s*"+({operation_name}[^"]+)"+""",
      """"+resourceGroupName"+:\s*"+({resource_group}[^"]+)"+""",
      """"+resourceProviderName"+:[^\}]+value"+:\s*"+({service_name}[^"]+)"+""",
      """"+resourceType"+:[^\}]+value"+:\s*"+({resource_type}[^"]+)"+""",
      """"+resourceId"+:\s*"+({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)"+""",
      """"+status"+:[^\}]+value"+:\s*"+({status}[^"]+)"+""",
      """"+subscriptionId"+:\s*"+({subscription_id}[^"]+)"+""",
      """"+tenantId"+:\s*"+({tenant_id}[^"]+)"+""",
      """"+properties[^\}]+statusMessage[^\}]+error[^\}]+code\\*"+:\s*\\+"+({result_code}[^\\]+)""",
      """"+properties[^\}]+statusMessage[^\}]+error[^\}]+message\\*"+:\s*\\+"+({failure_reason}[^"]+)\\""",
      
}
```