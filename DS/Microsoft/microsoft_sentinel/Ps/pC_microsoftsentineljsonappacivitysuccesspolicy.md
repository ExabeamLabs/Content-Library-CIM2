#### Parser Content
```Java
{
Name = microsoft-sentinel-json-app-acivity-success-policy
    ParserVersion = v1.0.0
    Conditions = [ """"Type":"BehaviorAnalytics"""", """"ActivityType":"Policy"""" ]

microsoft-sentinel-app-notificatation-json = {
    Vendor = Microsoft
    Product =  Microsoft Sentinel
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """exa_json_path=$.time,exa_field_name=time""",
      """exa_json_path=$.callerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.operationName,exa_field_name=operation""",
      """exa_json_path=$.resourceId,exa_field_name=resource_id""",
      """exa_json_path=$.resourceId,exa_regex=\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)"""
      """exa_json_path=$.level,exa_field_name=severity""",
      """exa_json_path=$.resultSignature,exa_field_name=result""",
      """exa_json_path=$.correlationId,exa_field_name=correlation_id"""
      """exa_json_path=$.category,exa_field_name=category""",
      """exa_json_path=$..eventCategory,exa_field_name=operation_type""",
      """exa_json_path=$..entity,exa_field_name=object""",
      """exa_json_path=$..statusCode,exa_field_name=result_code""",
      """exa_json_path=$.category,exa_field_name=category""",
      """exa_json_path=$.identity.claims.aud,exa_field_name=aud""",
      """exa_json_path=$.identity.claims.iss,exa_field_name=iss""",
      """exa_json_path=$.identity.claims.iat,exa_field_name=iat""",
      """exa_json_path=$.identity.claims.nbf,exa_field_name=nbf""",
      """exa_json_path=$.identity.claims.exp,exa_field_name=exp""",
      """exa_json_path=$.identity.claims.aio,exa_field_name=aio""",
      """exa_json_path=$.identity.claims.appid,exa_field_name=app_id""",
      """exa_json_path=$.identity.claims.appidacr,exa_field_name=app_id_acr""",
      """exa_json_path=$.identity.claims.uti,exa_field_name=uti""",
      """exa_json_path=$.identity.claims.ver,exa_field_name=version""",
      """exa_json_path=$.authorization.scope,exa_field_name=authorization_scope"""
    
}
```