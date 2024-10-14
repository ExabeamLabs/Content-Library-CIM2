#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-auditevent
  Vendor = Microsoft
  Product = Azure Key Vault
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"callerIpAddress":""", """MICROSOFT.KEYVAULT""", """"operationName":""" ]
  Fields = [
    """exa_json_path=$.id,exa_field_name=alert_id""",
    """exa_json_path=$..time,exa_field_name=time""",
    """exa_json_path=$.category,exa_field_name=operation_type""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.resultType,exa_field_name=result""",
    """exa_json_path=$.correlationId,exa_field_name=correlation_id""",
    """exa_json_path=$.callerIpAddress,exa_field_name=src_ip""",
    """exa_json_path=$.resourceId,exa_regex=\s*"+({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)"+""",
    """exa_json_path=$.operationVersion,exa_field_name=operation_version""",
    """exa_json_path=$.resultSignature,exa_field_name=result_code""",
    """exa_json_path=$.durationMs,exa_field_name=duration"""
    """exa_json_path=$..httpStatusCode,exa_field_name=http_response_code""",
    """exa_json_path=$..requestUri,exa_field_name=url""",
    """exa_json_path=$.identity.claim.appid,exa_field_name=app_id"""
    """exa_json_path=$..clientInfo,exa_field_name=user_agent"""
    """exa_json_path=$.properties,exa_field_name=properties"""
    """exa_regex="claims":.+?idtyp":"user".+?name":"({full_name}[^"]+)"""
    """exa_regex=claims".+?"http:.+?identity\/claims\/name":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```