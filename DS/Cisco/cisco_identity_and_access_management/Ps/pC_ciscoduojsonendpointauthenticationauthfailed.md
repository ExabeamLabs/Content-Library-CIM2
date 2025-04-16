#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-authfailed
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [""""server_section":""", """"auth_stage":""", """authentication"""]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time"""
    """exa_regex=\sdvchost=({host}[\w\-.]+)\s\w+=""",
    """exa_json_path=$.hostname,exa_field_name=host"""
    """exa_json_path=$.username,exa_field_name=user"""
    """exa_json_path=$.status,exa_field_name=action"""
    """exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.auth_stage,exa_field_name=auth_method"""
    """exa_regex=(("status":\s*"Reject"[^\}]*"msg":\s*"({failure_reason}[^"]+))|("msg":\s*"({additional_info}[^"]+)))""""

  ]
  ParserVersion = "v1.0.0"


}
```