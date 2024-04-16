#### Parser Content
```Java
{
Name = microsoft-azure-json-file-success-1
   Vendor = Microsoft
   ParserVersion = v1.0.0
   TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
   Conditions = [ """Type":"StorageBlobLogs""", """OperationName""" ] 
 
azure-workspaceblob-json = {
    Vendor = Microsoft
    Product = Azure Monitor
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
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
    """"+CallerIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"+""",
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