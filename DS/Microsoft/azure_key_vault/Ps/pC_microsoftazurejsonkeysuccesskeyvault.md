#### Parser Content
```Java
{
Name = microsoft-azure-json-key-success-keyvault
   Vendor = Microsoft
   Product = Azure Key Vault
   ParserVersion = v1.0.0
   TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"""
   Conditions = [ """Type":"AzureDiagnostics""", """ResourceProvider":"MICROSOFT.KEYVAULT""", """OperationName""" ] 
   Fields = [
    """"+TimeGenerated"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z?)"+""",
    """"+TenantId"+:\s*"+({tenant_id}[^"]+)"+""",
    """"+OperationName"+:\s*"+({operation}[^"]+)"+""",
    """"+CorrelationId"+:\s*"+({correlation_id}[^"]+)"+""",
    """"+OperationVersion"+:\s*"+({operation_version}[^"]+)"+""",
    """"+Category"+:\s*"+({operation_type}[^"]+)"+""",
    """"+Type"+:\s*"+({event_category}[^"]+)"+""",
    """"+ResourceId"+:\s*"+({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)"+""",
    """"+ResultType"+:\s*"+({result_code}[^"]+)"+""",
    """"+ResultDescription"+:\s*"+({failure_reason}[^:"]+?)(\\+)?\w+:""",
    """"+Resource"+:\s*"+({resource_name}[^"]+)"+""",
    """"+ResourceGroup"+:\s*"+({resource_group}[^"]+)"+""",
    """"+ResourceProvider"+:\s*"+({service_name}[^"]+)"+""",
    """"+SubscriptionId"+:\s*"+({subscription_id}[^"]+)"+""",
    """"+ResourceType"+:\s*"+({resource_type}[^"]+)"+""",
    """"+requestUri_s"+:\s*"+({url}[^"]+)"+""",
    """"+CallerIPAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?"+""",
    """"+id_s"+:\s*"+({creds_path}[^"]+\/({creds_name}[^\/"]+)|[^"]+)"+""",
    """"+clientInfo"+:\s*"+({user_agent}[^"]+)"+""",
    """"+clientInfo_s"+:\s*"+({user_agent}[^"]+)"+""",
    """"+identity_claim_upn_s"+:\s*"+({email_address}[^"]+@({email_domain}[^"]+))""",
    """"+keyProperties_type_s"+:\s*"+({key_type}[^"]+)"+""",
    """"+(R|r)esourceId"+:"+({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?\/[^"]+)""""
    """"httpStatusCode_d"+:"+({http_response_code}\d+)"""",
    """({app}MICROSOFT.KEYVAULT)"""
    ]
    DupFields = [ "operation->operation_name", "resource_name->keyvault"]
 

}
```