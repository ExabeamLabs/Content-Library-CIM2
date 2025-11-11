#### Parser Content
```Java
{
Name = cisco-fp-json-alert-trigger-success-502
  Vendor = Cisco
  Product = Cisco Network Security
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"protocol":""", """"recordType": 502,""", """blockLength""", """"recordTypeDescription":""" ]
  Fields = [
    """exa_json_path=$.connectionTimestamp,exa_regex=({time}\d{10})""",
    """exa_json_path=$.@computed.sensor,exa_field_name=host""",
    """exa_json_path=$.sourceIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationIpAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.fileSize,exa_field_name=bytes""",
    """exa_json_path=$.@computed.recordTypeDescription,exa_field_name=alert_name""",
    """exa_json_path=$.@computed.recordTypeDescription,exa_field_name=alert_type""",
    """exa_json_path=$.@computed.filePolicy,exa_field_name=rule""",
    """exa_json_path=$.destinationPort,exa_field_name=dest_port""",
    """exa_json_path=$.sourcePort,exa_field_name=src_port""",
    """exa_json_path=$.@computed.clientApplication,exa_field_name=process_path""",
    """exa_json_path=$.@computed.clientApplication,exa_field_name=process_name""",
    """exa_json_path=$.shaHash,exa_regex=^(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))$""",
    """exa_json_path=$.uri.data,exa_field_name=malware_url""",
    """exa_json_path=$.fileName.data,exa_field_name=malware_file_name""",
    """exa_json_path=$.direction,exa_field_name=direction""",
    """exa_json_path=$.@computed.fileType,exa_field_name=file_type""",
    """exa_json_path=$.@computed.user,exa_regex=(No Authentication Required|Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.disposition,exa_field_name=result""",
    """exa_json_path=$.@computed.disposition,exa_field_name=additional_info""",
    """exa_json_path=$.threatScore,exa_field_name=alert_severity""",
    """exa_json_path=$.recordType,exa_field_name=record_type"""
  ]


}
```