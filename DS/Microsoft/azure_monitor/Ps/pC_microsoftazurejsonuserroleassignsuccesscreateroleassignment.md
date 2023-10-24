#### Parser Content
```Java
{
Name = microsoft-azure-json-user-role-assign-success-createroleassignment
  ParserVersion = v1.0.0
  Conditions = [ """localizedValue":"Create role assignment""" ]
  Fields = ${MSParserTemplates.azure-activity-json.Fields} [
    """"+requestbody"+:[^\}]+"+Id\\?"+:\s*\\?"+({assignment_id}[^"]+)\\"+""",
    """"+requestbody"+:[^\}]+"+PrincipalId\\?"+:\s*\\?"+({principal_id}[^"]+)\\"+""",
    """"+requestbody"+:[^\}]+"+PrincipalType\\?"+:\s*\\?"+({principal_type}[^"]+)\\"+""",
    """"+requestbody"+:[^\}]+"+RoleDefinitionId\\?"+:\s*\\?"+({role_definition_id}[^"]+)\\"+""",
  ]

azure-activity-json = {
    Vendor = Microsoft
    Product = Azure Monitor
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    Fields = [
      """"+eventTimestamp"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+""",
      """"+authorization"+:[^\}]+scope"+:\s*"+({authorization_scope}[^"]+)""", 
      """"+caller"+:\s*"+({email_address}[^"]+@({email_domain}[^"]+))""",
      """"+claims"+:[^\}]+ipaddr"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"+""",
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