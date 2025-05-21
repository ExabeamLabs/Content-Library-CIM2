#### Parser Content
```Java
{
Name = cribl-cribl-json-app-activity-catchall
  Vendor = Cribl
  Product = Cribl
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """"time":""", """cid":""", """"level":""", """"ioType":""", """"ioName":""", """"message":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.channel,exa_field_name=channel""",
    """exa_json_path=$.level,exa_field_name=severity""",
    """exa_json_path=$.message,exa_field_name=additional_info""",
    """exa_json_path=$..bucket,exa_field_name=bucket_name"""
    """exa_regex="file":"(({file_path}[^"]*\/)?({file_name}[^"]+))"""
    """exa_json_path=$..receiveCount,exa_field_name=count"""
    """exa_json_path=$..messageId,exa_field_name=msg_id"""
    """exa_json_path=$..serviceId,exa_field_name=service_id"""
    """exa_json_path=$..errorCode,exa_field_name=failure_reason"""
    """exa_json_path=$..region,exa_field_name=region"""
    """exa_json_path=$..port,exa_field_name=src_port"""
    """exa_json_path=$.credentials..endpoint.hostname,exa_field_name=host"""
    """exa_json_path=$.src,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = ["additional_info-> event_name"]
  ParserVersion = v1.0.0


}
```