#### Parser Content
```Java
{
Name = tenable-t-json-endpoint-scan-scaninformation
  ParserVersion = v1.0.0
  Product = Tenable Web App Scanning
  Vendor = Tenable
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" , "yyyy-MM-dd'T'HH:mm:ssZ" ]
  ExtractionType = json
  Conditions = [ """"synopsis":""", """"scan":""",""""plugin":""", """"WAS_FINDING""" ]
  Fields = [
   """exa_json_path=$.updates[0].plugin.synopsis,exa_field_name=alert_name""",
   """exa_json_path=$.updates[0].severity,exa_field_name=alert_severity""",
   """exa_json_path=$.updates[0].plugin.description,exa_field_name=additional_info""",
   """exa_json_path=$.updates[0].output,exa_field_name=result""",
   """exa_json_path=$.updates[0].asset.fqdn,exa_field_name=web_domain""",
   """exa_json_path=$.updates[0].asset.uuid,exa_field_name=user_uid""",
   """exa_json_path=$.updates[0].scan.uuid,exa_field_name=scan_id""",
   """exa_json_path=$.updates[0].first_found,exa_field_name=time""",
   """exa_json_path=$.updates[0].http_method,exa_field_name=method""",
   """exa_json_path=$.updates[0].cve,exa_field_name=cve_id"""
  ]


}
```