#### Parser Content
```Java
{
Name = "zscaler-ia-json-app-login-success-sessionstatus"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Private Access"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  ExtractionType = json
  Conditions = [""""SessionStatus":""" , """"TimestampAuthentication":""" , """"CertificateCN":""",""""ZEN":"""]
  Fields = [
     """exa_json_path=$.LogTimestamp,exa_regex=({time}\w{3}\s+\d{2}\s+(\d{2}:){2}\d{2}\s+\d{4})"""
     """exa_json_path=$.SessionStatus,exa_field_name=result""",
     """exa_json_path=$.Username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?)"|({full_name}[^",]+))"""
     """exa_json_path=$.TotalBytesRx,exa_field_name=bytes_in""",
     """exa_json_path=$.TotalBytesTx,exa_field_name=bytes_out""",
     """exa_json_path=$.PublicIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """exa_json_path=$.Hostname,exa_regex=^({host}[\w.-]+)$"""
     """exa_json_path=$.ClientType,exa_field_name=client_type""",
     """exa_json_path=$.PrivateIP,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
     """exa_json_path=$.FQDNRegisteredError,exa_regex=({error_code}.+?)"""
     ]


}
```