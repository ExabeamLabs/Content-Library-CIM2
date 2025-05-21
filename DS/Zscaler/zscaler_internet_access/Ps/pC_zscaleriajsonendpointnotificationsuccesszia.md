#### Parser Content
```Java
{
Name = zscaler-ia-json-endpoint-notification-success-zia
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """"category":"""",""""interface":"""",""""auditlogtype":"ZIA"""",""""adminid":"""", ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.resource,exa_field_name=resource""",
    """exa_json_path=$.interface,exa_field_name=interface""",
    """exa_json_path=$.adminid,exa_field_name=admin_id""",
    """exa_json_path=$.clientip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.result,exa_field_name=result""",
    """exa_json_path=$.errorcode,exa_field_name=error_code""",
  ]


}
```