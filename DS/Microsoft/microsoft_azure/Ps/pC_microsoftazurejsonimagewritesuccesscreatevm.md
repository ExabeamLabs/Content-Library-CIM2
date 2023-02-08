#### Parser Content
```Java
{
Name = microsoft-azure-json-image-write-success-createvm
  Vendor = Microsoft
  Product = Microsoft Azure
  ParserVersion = v1.0.0
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  Conditions = [ """localizedValue":"Create or Update Virtual Machine""" ]
  Fields = ${MSParserTemplates.azure-activity-json.Fields} [
    """"+responseBody"+:[^\}]+"+name\\?"+:\s*\\?"+({resource_name}[^"]+)\\"+""",
    """"+responseBody"+:[^\}]+"+location\\?"+:\s*\\?"+({region}[^"]+)\\"+""",
    """"+responseBody"+:[^\}]+"+vmId\\?"+:\s*\\?"+({instance_id}[^"]+)\\"+""",
    """"+responseBody"+:[^\}]+"+vmSize\\?"+:\s*\\?"+({vm_size}[^"]+)\\"+""",
    """"+imageReference\\?"+:[^\}]+"+publisher\\?"+:\s*\\?"+({image_publisher}[^"]+)\\"+"""
    """"+imageReference\\?"+:[^\}]+"+offer\\?"+:\s*\\?"+({image_name}[^"]+)\\"+""",
    """"+imageReference\\?"+:[^\}]+"+sku\\?"+:\s*\\?"+({image_release}[^"]+)\\"+""",
    """"+imageReference\\?"+:[^\}]+"+exactVersion\\?"+:\s*\\?"+({image_version}[^"]+)\\"+""",
    """"+osDisk\\?"+:[^\}]+"+osType\\?"+:\s*\\?"+({os_type}[^"]+)\\"+""",
    """"+osDisk\\?"+:[^\}]+"+createOption\\?"+:\s*\\?"+({source_resource_type}[^"]+)\\"+""",
    """"+osProfile\\?"+:[^\}]+"+computerName\\?"+:\s*\\?"+({computer_name}[^"]+)\\"+""",
    """"+osProfile\\?"+:[^\}]+"+adminUsername\\?"+:\s*\\?"+({os_admin}[^"]+)\\"+""",
    """"+networkInterfaces\\?"+:[^\}]+"+id\\?"+:\s*\\?"+({interface_id}[^"]+)\\"+""",
  ]
  DupFields = [ "image_name->source_resource" ]

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