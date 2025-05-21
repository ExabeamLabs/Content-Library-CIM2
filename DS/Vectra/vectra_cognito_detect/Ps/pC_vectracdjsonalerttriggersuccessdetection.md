#### Parser Content
```Java
{
Name = vectra-cd-json-alert-trigger-success-detection
  Vendor = Vectra
  Product = Vectra Cognito Detect
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  time_createdFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
  start_timeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"detection":""",""""threat":""",""""grouped_details":""",""""detection_url":""", """"certainty":""", """"detection_type":""", """"type":""" ]
  Fields =[
  	"""exa_json_path=$.last_timestamp,exa_field_name=time""",
  	"""exa_json_path=$.note,exa_field_name=event_name""",
  	"""exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  	"""exa_json_path=$.grouped_details[:1].src_host.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  	"""exa_json_path=$.src_host.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  	"""exa_json_path=$.detection_url,exa_field_name=threat_url""",
  	"""exa_json_path=$.src_host.name,exa_regex=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+))$""",
  	"""exa_json_path=$..src_accounts[:1].name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
  	"""exa_json_path=$.detection,exa_field_name=alert_name""",
  	"""exa_json_path=$.detection_type,exa_field_name=alert_type""",
  	"""exa_json_path=$.threat,exa_field_name=alert_severity""",
  	"""exa_json_path=$.detection_category,exa_field_name=threat_category""",
  	"""exa_json_path=$.grouped_details[:1].sessions,exa_field_name=more_info""",
  	"""exa_json_path=$.grouped_details[:1].service_accesses,exa_field_name=more_info""",
  	"""exa_json_path=$..summary.description,exa_field_name=additional_info""",
  	"""exa_json_path=$.grouped_details[:1].bytes_received,exa_field_name=bytes_in""",
  	"""exa_json_path=$.grouped_details[:1].bytes_sent,exa_field_name=bytes_out""",
  	"""exa_json_path=$.grouped_details[:1].dst_ports[:1],exa_field_name=dest_port""",
  	"""exa_json_path=$.grouped_details[:1].dst_ips[:1],exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  	"""exa_json_path=$.data_source.connection_id,exa_field_name=connection_id""",
    """exa_json_path=$.data_source.type,exa_field_name=alert_source""",
    """exa_json_path=$..sensor_name,exa_field_name=sensor_name""",
    """exa_json_path=$..sensor,exa_field_name=sensor""",
    """exa_json_path=$..summary.operations[:1],exa_field_name=operation""",
    """exa_json_path=$..summary.reasons[:1],exa_field_name=alert_reason""",
    """exa_json_path=$.id,exa_field_name=alert_id""",
    """exa_json_path=$.url,exa_field_name=url""",
    """exa_json_path=$.state,exa_field_name=state""",
    """exa_json_path=$.created_timestamp,exa_field_name=time_created""",
    """exa_json_path=$.src_account.id,exa_field_name=account_id""",
    """exa_json_path=$..summary.suspicious_flow_connectors[:1],exa_field_name=connectors""",
    """exa_json_path=$.src_account.name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.src_account.privilege_level,exa_field_name=user_privilege_level""",
    """exa_json_path=$.src_account.privilege_category,exa_field_name=user_privilege_category""",
    """exa_json_path=$.src_account.certainty,exa_field_name=user_threat_certainty""",
    """exa_json_path=$.src_account.threat,exa_field_name=user_threat_level""",
    """exa_json_path=$.src_account.url,exa_field_name=user_url""",
    """exa_json_path=$..src_accounts[:1].privilege_level,exa_field_name=user_privilege_level""",
    """exa_json_path=$..src_accounts[:1].privilege_category,exa_field_name=user_privilege_category""",
    """exa_json_path=$.first_timestamp,exa_field_name=start_time"""
  ]
  ParserVersion = "v1.0.0"
 

}
```