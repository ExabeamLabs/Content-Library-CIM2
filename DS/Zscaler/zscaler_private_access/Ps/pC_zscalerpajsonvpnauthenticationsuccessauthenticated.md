#### Parser Content
```Java
{
Name = "zscaler-pa-json-vpn-authentication-success-authenticated"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
ParserVersion = "v1.0.0"
TimeFormat = "MMM dd HH:mm:ss yyyy"
ExtractionType = json
Conditions = [
  """"ZEN":""",
  """"SessionStatus":""",
  """"ZPN_STATUS_AUTHENTICATED""""
]
Fields = [
  """exa_json_path=$.LogTimestamp,exa_regex=({time}\w{3}\s*\d+\s+\d\d:\d+:\d+\s\d\d\d\d)""",
  """exa_json_path=$.SessionID,exa_field_name=session_id,exa_match_expr=!InList(toLower($.SessionID),"")""",
  """exa_json_path=$.PublicIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.PublicIP,exa_regex=({src_translated_ip}[A-Fa-f\d:.]+)"""
  """exa_json_path=$.TotalBytesRx,exa_field_name=bytes_in"""
  """exa_json_path=$.TotalBytesTx,exa_field_name=bytes_out"""
  """exa_json_path=$.SessionStatus,exa_field_name=event_name"""
]


}
```