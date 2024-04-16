#### Parser Content
```Java
{
Name = "hp-lprinter-json-printer-activity-success-laserjet"
ExtractionType = json
Vendor = "HP"
Product = "HP LaserJet Printer"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""LaserJet"""
"""job_lab_ntusername"""
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time""",
  """exa_json_path=$.host,exa_field_name=host""",
  """exa_json_path=$.job_lab_ntusername,exa_regex=^(?:Unspecified|({user}[\w\.\-]{1,40}\$?))""",
  """exa_json_path=$.job_lab_documentname,exa_regex=^(?:Unspecified|({object}[^"]+))""",
  """exa_json_path=$.job_qty_size,exa_field_name=bytes""",
  """exa_json_path=$.job_qty_printedpages,exa_field_name=num_pages""",
  """exa_json_path=$.printer_lab_localname,exa_field_name=printer_name""",
  """exa_json_path=$.printer_lab_ipaddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.port,exa_field_name=src_port"""
  """exa_json_path=$.job_lab_ntusermachine,exa_regex=^(?:Unspecified|({src_host}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```