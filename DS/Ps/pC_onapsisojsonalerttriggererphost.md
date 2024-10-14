#### Parser Content
```Java
{
Name = onapsis-o-json-alert-trigger-erphost
    Vendor=Onapsis
    Product=Onapsis
    ParserVersion = "v1.0.0"
    ExtractionType = json
    TimeFormat="yyyy-MM-dd'T'HH:mm:ss"
    Conditions=[ """"alarm_name":""", """"erp_host":""", """"incident_detail":""", """"incident_name": "Extraction problem detected in ICM: Extractors Adjusted"""  ]
    Fields=[
      """exa_json_path=$.created_at,exa_field_name=time""",
      """exa_json_path=$.username,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """exa_json_path=$.incident_name,exa_field_name=event_name""",
      """exa_json_path=$..alarm_name,exa_field_name=alert_name""",
      """exa_json_path=$.incident_detail,exa_field_name=additional_info""",
      """exa_json_path=$.src,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.source_port,exa_field_name=src_port""",
      """exa_json_path=$.dst,exa_regex=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^"]+))""",
      """exa_json_path=$.destination_port,exa_field_name=dest_port""",
      """exa_json_path=$.severity,exa_field_name=alert_severity""",
]


}
```