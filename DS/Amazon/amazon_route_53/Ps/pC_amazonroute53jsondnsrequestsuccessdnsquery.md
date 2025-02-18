#### Parser Content
```Java
{
Name = amazon-route53-json-dns-request-success-dnsquery
 Vendor = Amazon
 Product = Amazon Route 53
 ExtractionType = json
 TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
 ParserVersion = v1.0.0
 Conditions = [""""rcode":""", """"srcids":""",  """"query_name":""", """"query_timestamp":""", """"query_class":""" ]
 Fields = [
   """exa_json_path=$.query_timestamp,exa_field_name=time""",
   """exa_json_path=$.srcaddr,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """exa_json_path=$.query_name,exa_field_name=dns_query""",
   """exa_json_path=$.query_type,exa_field_name=dns_query_type""",
   """exa_json_path=$.rcode,exa_field_name=dns_response_code""",
   """exa_json_path=$.srcport,exa_field_name=src_port""",
   """exa_json_path=$.query_class,exa_field_name=dns_query_flags"""
   """exa_json_path=$.account_id,exa_field_name=account_id"""
   """exa_json_path=$.region,exa_field_name=region"""
   """exa_json_path=$.vpc_id,exa_field_name=vpc"""
   """exa_json_path=$..instance,exa_field_name=instance_id"""
   """exa_json_path=$.transport,exa_field_name=protocol"""
   """exa_json_path=$.answers,exa_field_name=dns_response"""
 ]


}
```