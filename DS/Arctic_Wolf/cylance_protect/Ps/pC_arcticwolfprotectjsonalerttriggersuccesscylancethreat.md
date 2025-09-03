#### Parser Content
```Java
{
Name = "arcticwolf-protect-json-alert-trigger-success-cylancethreat"
Vendor = "Arctic Wolf"
Product = "Cylance Protect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [
"""destinationServiceName =Cylance Protect"""
"""dproc=threats"""
""""device_name":"""
"""cylance_score"""
]
Fields = [
    """exa_json_path=$.file_path,exa_regex=({file_path}({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s"]+))?))("|$)"""
    """exa_json_path=$.sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.ip_address,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.classification,exa_field_name=alert_type"""
    """exa_json_path=$.file_size,exa_field_name=bytes"""
    """exa_json_path=$.device_name,exa_field_name=host"""
    """exa_json_path=$.mac_address,exa_field_name=src_mac"""
    """exa_json_path=$.cylance_score,exa_field_name=malware_score"""
    """exa_json_path=$.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.found_on_device,exa_field_name=time"""
]
ParserVersion = "v1.0.0"


}
```