#### Parser Content
```Java
{
Name = sap-s-json-app-activity-success-eventtype
  Product = SAP
  Conditions = [ """"CURRENT_TIMESTAMP":""", """"UTCDIFF":""", """"EVENT_TYPE":""", """"EVENT_SUBTYPE":""" ]
  ParserVersion = "v1.0.0"

sap-events-2 = {
    Vendor = SAP
    Product = SAP
    ExtractionType = json
    TimeFormat = "yyyyMMddHHmmss"
    Fields = [
      """exa_json_path=$.CURRENT_TIMESTAMP,exa_field_name=time""",
      """exa_json_path=$.EVENT_TYPE,exa_field_name=event_name""",
      """exa_json_path=$.ALGUSER,exa_field_name=user""",
      """exa_json_path=$.ALGTEXT,exa_field_name=additional_info""",
      """exa_json_path=$.ALGLTERM,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.ALGSYSTEM,exa_field_name=src_host""",
      """exa_json_path=$.TXSEVERITY,exa_field_name=severity""",
      """exa_json_path=$.TXSUBCLSID,exa_field_name=operation"""
    
}
```