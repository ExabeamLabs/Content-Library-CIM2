#### Parser Content
```Java
{
Name = pan-ngfw-json-app-notification-success-auth
 Conditions = [ """"LogType":"SYSTEM"""", """"Subtype":"auth"""", """"EventName":"saml-client-redirect""""]
 Fields = ${DLPaloAltoParserTemplates.json-pan-system.Fields}[
    """exa_json_path=$.EventDescription,exa_regex=Client '({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))' redirected to"""
    """exa_regex=({operation}saml-client-redirect)""",
 ]

json-pan-system = {
    Vendor = Palo Alto Networks
    Product = Palo Alto NGFW
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    ExtractionType = json
    Fields = [
      """exa_json_path=$.EventTime,exa_field_name=time""",
      """exa_json_path=$.LogSourceName,exa_regex=^({host}[\w.-]+)$""",
      """exa_json_path=$.Subtype,exa_field_name=subtype""",
      """exa_json_path=$.VendorSeverity,exa_field_name=severity""",
      """exa_json_path=$.EventDescription,exa_field_name=additional_info""",
      """exa_json_path=$.SourceIP,exa_field_name=src_ip""",
      """exa_json_path=$.SourceUser,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_regex=({event_category}SYSTEM)"""
      """exa_json_path=$.event.VendorSeverity,exa_field_name=severity""",
      """exa_json_path=$.event.EventTime,exa_field_name=time""",
      """exa_json_path=$.event.LogSourceName,exa_regex=^({host}[\w.-]+)$""",
      """exa_json_path=$.event.Subtype,exa_field_name=subtype""",
      """exa_json_path=$.event.EventDescription,exa_field_name=additional_info""",
      """exa_json_path=$..DeviceName,exa_regex=^({host}[\w.-]+)$"""
      """exa_json_path=$..DeviceName,exa_field_name=device_name"""
      
}
```