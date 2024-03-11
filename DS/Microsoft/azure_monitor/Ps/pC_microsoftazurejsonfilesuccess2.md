#### Parser Content
```Java
{
Name = microsoft-azure-json-file-success-2
   Vendor = Microsoft
   ParserVersion = v1.0.0
   TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
   Conditions = [ """serviceType":"blob""", """operationName""" ] 
 
azure-classicblob-json = {
    Vendor = Microsoft
    Product = Azure Monitor
    TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
    Fields = [
    """"+time"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+""",
    """"+resourceId"+:\s*"+({resource}[^"]+)"+""",
    """"+category"+:\s*"+({operation_type}[^"]+)"+""",
    """"+operationName"+:\s*"+({operation}[^"]+)"+""",
    """"+operationVersion"+:\s*"+({operation_version}[^"]+)"+""",
    """"+schemaVersion"+:\s*"+({schema_version}[^"]+)"+""",
    """"+statusCode"+:\s*({result_code}[^,"]+)""",
    """"+statusText"+:\s*"+({result}[^"]+)"+""",
    """"+callerIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"+""",
    """"+correlationId"+:\s*"+({correlation_id}[^"]+)"+""",
    """"+identity"+:[^\}]+"+type"+:\s*"+({auth_type}[^"]+)"+""",
    """"+location"+:\s*"+({region}[^"]+)"+""",
    """"+properties"+:[^\}]+"+accountName"+:\s*"+({storage_account}[^"]+)"+""",
    """"+properties"+:[^\}]+"+userAgentHeader"+:\s*"+({user_agent}[^"]+)"+""",
    """"+properties"+:[^\}]+"+lastModifiedTime"+:\s*"+({file_modify_time}[^"]+)"+""",
    """"+properties"+:[^\}]+"+requestBodySize"+:\s*({bytes_in}\d+)""",
    """"+properties"+:[^\}]+"+responseBodySize"+:\s*({bytes_out}\d+)""",
    """"+uri"+:\s*"+({file_path}[^"]+)"+""",
    """"+protocol"+:\s*"+({protocol}[^"]+)"+""",
    """"+resourceType"+:\s*"+({resource_type}({service_name}[^"\/]+)\/[^"]+)"+""",
    ]
    DupFields = [ "operation->operation_name", "storage_account->dest_host" 
}
```