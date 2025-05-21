#### Parser Content
```Java
{
Name = "qualys-q-json-app-activity-success-scan"
Vendor = "Qualys"
Product = "Qualys AssetView"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """"Severity":""",""""IP Address":""","""Last VM Scanned Date":""",""""Last Update Datetime":""" ]
Fields = [
  """exa_json_path=$.['Last Update Datetime'],exa_field_name=time""",
  """exa_json_path=$.Port,exa_field_name=src_port,exa_match_expr=!Contains($.Port,"-")""",
  """exa_json_path=$.Severity,exa_field_name=alert_severity""",
  """exa_json_path=$.['Netbios Name'],exa_field_name=src_host""",
  """exa_json_path=$.['IP Address'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.Protocol,exa_field_name=protocol,exa_match_expr=!Contains($.Protocol,"-","NaN")""",
  """exa_regex="Status":"(NaN|-|({result}[^"]+))"""",
  """exa_json_path=$.Results,exa_field_name=additional_info,exa_match_expr=!Contains($.Results,"-")""",
  """exa_json_path=$.QID,exa_field_name=alert_id,exa_match_expr=!Contains($.QID,"-")""",
  """exa_json_path=$.['Operating System'],exa_field_name=os"""  
]
ParserVersion = "v1.0.0"


}
```