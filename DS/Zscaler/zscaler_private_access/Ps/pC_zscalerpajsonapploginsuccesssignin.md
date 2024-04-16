#### Parser Content
```Java
{
Name = zscaler-pa-json-app-login-success-signin
  ParserVersion = "v1.0.0"
  Conditions = [ """"AuditOperationType":"Sign In"""", """"User":"""", """"ObjectType":"Authentication"""" ]
  Fields = ${DLZscalerParsersTemplates.zscaler-audit-events.Fields} [
      """exa_json_path=$.AuditNewValue,exa_regex="remoteIP\\?":\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?""""
  ]

zscaler-audit-events = {
    Vendor = Zscaler
    Product = Zscaler Private Access
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields = [
      """exa_json_path=$.CreationTime,exa_field_name=time""",
      """exa_json_path=$.User,exa_regex=(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))"""
      """exa_json_path=$.ObjectName,exa_field_name=object,exa_match_expr=!InList($.ObjectName,"")"""
      """exa_json_path=$.ObjectType,exa_field_name=object_type""",
      """exa_json_path=$.SessionID,exa_field_name=session_id,exa_match_expr=!InList($.SessionID,"")"""
      """exa_json_path=$.AuditOperationType,exa_field_name=event_name""",
# customer_id is removed
      """exa_json_path=$.AuditNewValue,exa_field_name=new_attribute,exa_match_expr=!InList($.AuditNewValue,"")"""
      """exa_json_path=$.AuditOldValue,exa_field_name=old_attribute,exa_match_expr=!InList($.AuditOldValue,"")"""
    
}
```