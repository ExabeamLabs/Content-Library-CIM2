#### Parser Content
```Java
{
Name = microsoft-azure-json-file-success-1
   Vendor = Microsoft
   Product = Microsoft Azure
   ParserVersion = v1.0.0
   TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
   Conditions = [ """Type":"StorageBlobLogs""", """OperationName""" ] 
 
azure-workspaceblob-json = {
    Vendor = Microsoft
    Product = Microsoft Azure
    TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
    Fields = [
    """"+TimeGenerated"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+""",
    """"+TenantId"+:\s*"+({tenant_id}[^"]+)"+""",
    """"+AccountName"+:\s*"+({storage_account}[^"]+)"+""",
    """"+Location"+:\s*"+({region}[^"]+)"+""",
    """"+Protocol"+:\s*"+({protocol}[^"]+)"+""",
    """"+OperationName"+:\s*"+({operation}[^"]+)"+""",
    """"+AuthenticationType"+:\s*"+({auth_type}[^"]+)"+""",
    """"+StatusCode"+:\s*"+({result_code}[^"]+)"+""",
    """"+StatusText"+:\s*"+({result}[^"]+)"+""",
    """"+Uri"+:\s*"+({url}({file_path}[^"]+\/({file_name}[^\?"]+))[^"]*|[^"]+)"+""",
    """"+CallerIpAddress"+:\s*"+({src_ip}[^"]+)"+""",
    """"+CorrelationId"+:\s*"+({correlation_id}[^"]+)"+""",
    """"+SchemaVersion"+:\s*"+({schema_version}[^"]+)"+""",
    """"+OperationVersion"+:\s*"+({operation_version}[^"]+)"+""",
    """"+UserAgentHeader"+:\s*"+({user_agent}[^"]+)"+""",
    """"+ReferrerHeader"+:\s*"+({referrer}[^"]+)"+""",
    """"+RequestBodySize"+:\s*({bytes_in}\d+)""",
    """"+ResponseBodySize"+:\s*({bytes_out}\d+)""",
    """"+LastModifiedTime"+:\s*"+({file_modify_time}[^"]+)"+""",
    """"+Category"+:\s*"+({operation_type}[^"]+)"+""",
    """"+Type"+:\s*"+({event_category}[^"]+)"+""",
    """"+RequesterUpn"+:\s*"+({email_address}[^"]+@({email_domain}[^"]+))""",
    ]
    DupFields = [ "operation->operation_name", "storage_account->dest_host" 
}
```