#### Parser Content
```Java
{
Name = tenable-t-json-endpoint-scan-scaninformation
  ParserVersion = v1.0.0
  Product = Tenable Web App Scanning
  Vendor = Tenable
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"synopsis":""", """"scan":""",""""plugin":""", """"WAS_FINDING""" ]
  Fields = [
   """exa_json_path=$..synopsis,exa_field_name=alert_name""",
   """exa_json_path=$..severity,exa_field_name=alert_severity""",
   """exa_json_path=$..description,exa_field_name=additional_info""",
   """exa_json_path=$.updates[*].output,exa_field_name=result""",
   """exa_json_path=$.updates[*].asset.fqdn,exa_field_name=web_domain""",
   """exa_json_path=$.updates[*].asset.uuid,exa_field_name=user_uid""",
   """exa_json_path=$.updates[*].scan.uuid,exa_field_name=scan_id""",
   """exa_json_path=$.updates[*].first_found,exa_field_name=time""",
   """exa_json_path=$.updates[*].http_method,exa_field_name=method""",
   """exa_json_path=$.updates[*].cve,exa_field_name=cve_id"""
  ]


}
```