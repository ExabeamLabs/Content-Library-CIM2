#### Parser Content
```Java
{
Name = "zscaler-pa-json-app-notification-connector-status"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
ParserVersion = "v1.0.0"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
ExtractionType = json
Conditions = [ """"ZEN":""", """"SessionType":""", """ZPN_ASSISTANT_""", """BROKER""", """"SessionStatus":""", """"Connector":""" ]
Fields = [
  """exa_json_path=$.LogTimestamp,exa_field_name=time""",
  """exa_json_path=$.SessionID,exa_field_name=session_id""",
  """exa_json_path=$.PublicIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.PrivateIP,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.TotalBytesRx,exa_field_name=bytes_in""",
  """exa_json_path=$.TotalBytesTx,exa_field_name=bytes_out""",
  """exa_json_path=$.SessionStatus,exa_field_name=event_name""",
  """exa_json_path=$.CountryCode,exa_field_name=src_country""",
  """exa_json_path=$.Connector,exa_field_name=host,exa_match_expr=!InList(toLower($.Connector),"0")"""
  """exa_json_path=$.Platform,exa_field_name=os"""
]


}
```