#### Parser Content
```Java
{
Name = sentinelone-scalyr-json-endpoint-notification-success-scalyragentlog
  Vendor = "SentinelOne"
  Product = "Scalyr"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"sca:RetentionType":""", """"account.id":""", """WARNING""", """"serverHost":""" , """"scalyrAgentLog"""" ]
  Fields = [
  	"""exa_json_path=$.timestamp,exa_field_name=time""",
  	"""exa_json_path=$.['account.id'],exa_field_name=account_id""",
  	"""exa_json_path=$.['account.name'],exa_field_name=account_name""",
  	"""exa_json_path=$.serverHost,exa_field_name=server_name""",
  	"""exa_json_path=$.serverIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  	"""exa_json_path=$.details,exa_field_name=additional_info""",
  	"""exa_json_path=$.logfile,exa_regex=({file_path}((|({file_dir}[^"]*?)[\\\/]+))?({file_name}[^"\\\/]+?(\.({file_ext}[^"\/\\\.]+))?))("|$)""",
  	"""exa_json_path=$.permissions,exa_regex=({file_permissions}\d+)""",
  	"""exa_regex=({severity}WARNING)"""
]
ParserVersion = "v1.0.0"


}
```