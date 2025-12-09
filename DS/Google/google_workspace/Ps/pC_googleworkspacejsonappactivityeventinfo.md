#### Parser Content
```Java
{
Name = google-workspace-json-app-activity-eventinfo
  ParserVersion = v1.0.0
  Conditions = [ """"source":""" , """"destination":""", """"service":""", """"message_info":""", """"event_info":""" ]

json-google-email-activity = {
  Vendor = Google
  Product = Google Workspace
  TimeFormat = ["epoch", "epoch_sec"]
  ExtractionType = json
  Fields = [
    """exa_json_path=$.event_info.timestamp_usec,exa_field_name=time""",
    """exa_json_path=$.event_info.success,exa_field_name=result""",
    """exa_json_path=$.event_info.mail_event_type,exa_field_name=category""",
    """exa_json_path=$.message_info.subject,exa_field_name=email_subject""",
    """exa_json_path=$.message_info.action_type,exa_field_name=result_code""",
    """exa_json_path=$.message_info.source.address,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.message_info.source.from_header_displayname,exa_field_name=log_source""",
    """exa_json_path=$.message_info.destination[*].address,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.message_info.destination[*].service,exa_field_name=action""",
    """exa_json_path=$.message_info.rfc2822_message_id,exa_field_name=message_id""",
    """exa_json_path=$.message_info.connection_info.client_ip,exa_field_name=src_ip""",
    """exa_json_path=$.message_info.connection_info.dkim_pass,exa_field_name=dkim_result""",
    """exa_json_path=$.message_info.connection_info.spf_pass,exa_field_name=spf_result""",
    """exa_json_path=$.message_info.connection_info.dmarc_pass,exa_field_name=dmarc_result""",
    """exa_json_path=$.message_info.num_message_attachments,exa_field_name=attachment_count""",
    """exa_json_path=$.message_info.attachment[*].file_name,exa_field_name=email_attachment""",
    """exa_json_path=$.message_info.payload_size,exa_field_name=bytes""",
    """exa_regex=destinationServiceName =(|({app}.+?))(\s+\w+=|\s*$)"""
  
}
```