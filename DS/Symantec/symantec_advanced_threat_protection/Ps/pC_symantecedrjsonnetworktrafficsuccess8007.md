#### Parser Content
```Java
{
Name = symantec-edr-json-network-traffic-success-8007
  ParserVersion = v1.0.0
  Conditions = [ """"product_name":"Symantec Endpoint""", """"type_id":8007""" ]
  Fields = ${SymantecParserTemplates.symantec-parser-template.Fields}[
    """"bytes_download":({bytes_in}\d+)""",
    """"direction_id":({direction}\d)""",
    """"dst_port":({dest_port}\d+)""",
    """"bytes_upload":({bytes_out}\d+)""",
    """dst_ip":\[?"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """src_ip":\[?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"type_id":({event_code}8007)""",
    """"size":({bytes}\d+)"""
  ]

symantec-parser-template = {
    Vendor = Symantec
    Product = Symantec Advanced Threat Protection
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"device_domain":"({domain}[^"]+)"""",
      """"device_name":"({src_host}[\w\-.]+)"""",
      """"device_os_name":"({os}[^"]+)"""",
      """"ipv4":\[?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"user_name":"({user}[\w\.\-]{1,40}\$?)"""",
      """"rule_description":"({additional_info}[^"]+?)\s*"""",
    
}
```