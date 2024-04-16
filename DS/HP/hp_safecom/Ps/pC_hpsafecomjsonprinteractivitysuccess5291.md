#### Parser Content
```Java
{
Name = hp-safecom-json-printer-activity-success-5291
ExtractionType = json
Vendor = "HP"
Product = "HP SafeCom"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"run_id""""
  """"print_size""""
  """"userid""""
  """"employee_cms_code""""
  """"day_of_week""""
]
Fields = [
    """exa_json_path=$.date_part,exa_field_name=time""",
    """exa_json_path=$.userid,exa_regex=^({user}[\w\.\-]{1,40}\$?)""",
    """exa_json_path=$.printer_name,exa_field_name=printer_name""",
    """exa_json_path=$.pages_printed,exa_field_name=num_pages""",
    """exa_json_path=$.document_details,exa_field_name=object""",
    """exa_json_path=$.employee_cms_code,exa_field_name=user_id""",
    """exa_json_path=$.print_size,exa_field_name=bytes"""
]
DupFields = [
  "printer_name->dest_host"
]
ParserVersion = "v1.0.0"


}
```