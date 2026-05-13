#### Parser Content
```Java
{
Name = microsoft-o365-json-user-permission-modify-success-adddelegatedpermission
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Operation":"Add delegated permission grant""", """"Workload":"""", """"ResultStatus":""""   ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"Operation":"({event_name}({operation}[^"]+))"""",
    """"ResultStatus":"({result}[^"]+)"""",
    """"Workload":"({app}[^"]+)"""",
    """\\\"User-Agent\\\":\\\"({user_agent}[^\"]+)\\\"""",
    """UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"UserKey":"({user_id}[^@\"]+)""",
    """ModifiedProperties":.+?"ServicePrincipal.DisplayName","NewValue":"({target}[^"]+)""",
    """ModifiedProperties":.+?"NewValue":"({target}[^"]+)","Name":"ServicePrincipal.DisplayName"""",
    """"NewValue":"({role_name}[^"]+)","Name":"AppRole.Value""",
    """"NewValue":"({role_id}[^"]+)","Name":"AppRole.Id""",
    """"Name":"AppRole.Value","NewValue":"({role_name}[^"]+)",""",
    """"Name":"AppRole.Id","NewValue":"({role_id}[^"]+)",""",
    """"OrganizationId":"({tenant_id}[^"]+)",""",
    """"extendedAuditEventCategory","Value":"({object}[^"]+)""",
    """"ServicePrincipal.ObjectID","NewValue":"({object_id}[^"]+)""",
    """ModifiedProperties":.+?"DelegatedPermissionGrant.Scope","NewValue":\s*"\s*({new_value}({permissions}[^"]+))","OldValue":\s*"(|({old_value}[^"]+))"""",
    """ModifiedProperties":.+?"OldValue":\s*"(|({old_value}[^"]+))","NewValue":\s*"\s*({new_value}({permissions}[^"]+))","Name":"DelegatedPermissionGrant.Scope""",
    """"NewValue":"({object_id}[^"]+)","Name":"ServicePrincipal.ObjectID""",
    """"Value":"({object}[^"]+)","Name":"extendedAuditEventCategory"""",
    """exa_json_path=$.CreationTime,exa_field_name=time""",
    """exa_json_path=$.Operation,exa_field_name=operation""",
    """exa_json_path=$.Operation,exa_field_name=event_name""",
    """exa_json_path=$.ResultStatus,exa_field_name=result""",
    """exa_json_path=$.Workload,exa_field_name=app""",
    """exa_regex=\\\"User-Agent\\\":\\\"({user_agent}[^\"]+)\\\"""",
    """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.UserKey,exa_regex=({user_id}[^@\"]+)""",
    """exa_json_path=$.OrganizationId,exa_field_name=tenant_id""",
    """exa_json_path=$.ModifiedProperties[?(@.Name == 'ServicePrincipal.DisplayName')].NewValue,exa_field_name=target"""
    """exa_json_path=$.ModifiedProperties[?(@.Name =='AppRole.Value')].NewValue,exa_field_name=role_name""",
    """exa_json_path=$.ModifiedProperties[?(@.Name =='AppRole.Id')].NewValue,exa_field_name=role_id""",
    """exa_json_path=$.ExtendedProperties[?(@.Name == 'extendedAuditEventCategory')].Value,exa_field_name=object""",
    """exa_json_path=$.ModifiedProperties[?(@.Name == 'ServicePrincipal.ObjectID')].NewValue,exa_field_name=object_id"""
    """exa_json_path=$.ModifiedProperties[?(@.Name == 'DelegatedPermissionGrant.Scope')].NewValue,exa_field_name=permissions"""
    """exa_json_path=$.ModifiedProperties[?(@.Name == 'DelegatedPermissionGrant.Scope')].NewValue,exa_field_name=new_value"""
    """exa_json_path=$.ModifiedProperties[?(@.Name == 'DelegatedPermissionGrant.Scope')].OldValue,exa_field_name=old_value"""
  ]


}
```