#### Parser Content
```Java
{
Name = cimcor-cimtrak-json-app-activity-success-catchall
  Vendor = Cimcor
  Product = CimTrak
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"logWebhookMsgVersion"""", """"time"""", """"user"""", """"cimTrakVersion"""", """"messageId"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_json_path=$.messageId,exa_field_name=message_id"""
    """exa_json_path=$.severity,exa_field_name=severity"""
    """exa_json_path=$.objectDetailId,exa_field_name=object_id""",
    """exa_json_path=$.objectType,exa_field_name=entity_type""",
    """exa_json_path=$.policyName,exa_field_name=policy_name""",
    """exa_json_path=$.policyId,exa_field_name=policy_id""",
    """exa_json_path=$.ipSrc,exa_field_name=src_ip"""
    """exa_json_path=$.fileName,exa_field_name=file_name""",
    """exa_json_path=$.path,exa_field_name=file_path""",
    """exa_json_path=$.hash,exa_field_name=file_hash""",
    """exa_json_path=$.processId,exa_field_name=process_id""",
    """exa_json_path=$.threadId,exa_field_name=thread_id""",
    """exa_json_path=$.reason,exa_field_name=result_reason"""
    """exa_json_path=$.rawMessage,exa_field_name=additional_info"""
    """exa_json_path=$.msgType,exa_field_name=event_subtype""",
    """exa_json_path=$.cimTrakVersion,exa_field_name=version"""
    """exa_regex="rawMessage":\s*"User[^"]+?'+({dest_user}[^']+)'+ was ({operation}added|deleted)"""
  ]


}
```