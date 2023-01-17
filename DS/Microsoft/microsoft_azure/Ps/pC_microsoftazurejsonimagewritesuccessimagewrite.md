#### Parser Content
```Java
{
Name = microsoft-azure-json-image-write-success-imagewrite
  Vendor = Microsoft
  Product = Microsoft Azure
  ParserVersion = v1.0.0
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  Conditions = [ """value":"Microsoft.Compute/images/write""" ]
  Fields = ${MSParserTemplates.azure-activity-json.Fields} [
    """"+responseBody"+:\s*"+\{[^\}\{]+"+name\\?"+:\s*\\?"+({resource_name}[^"]+)\\"+""",
    """"+responseBody"+:\s*"+\{[^\}\{]+"+location\\?"+:\s*\\?"+({region}[^"]+)\\"+""",
    """"+osDisk\\?"+:\s*\{[^\}\{]+"+osType\\?"+:\s*\\?"+({os_type}[^"]+)\\"+""",
    """"+osDisk\\?"+:\s*\{[^\}\{]+"+blobUri\\?"+:\s*\\?"+({source_resource}[^"]+)\\"+""",
  ]

azure-activity-json = {
    Vendor = Microsoft
    Product = Microsoft Azure
    TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
    Fields = [
      """"+eventTimestamp"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+""",
      """"+authorization"+:[^\}]+scope"+:\s*"+({auth_scope}[^"]+)""", 
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