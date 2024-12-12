#### Parser Content
```Java
{
Name = "github-g-json-app-activity-success-code_scanning"
    Vendor = "GitHub"
    Product = "GitHub"
    TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
    ExtractionType = json
    Conditions = [ """"alert_number":""", """"action":""", """"code_scanning""" ]
    Fields = [
        """exa_json_path=$.ref,exa_field_name=additional_info"""
        """exa_json_path=$.alert_number,exa_field_name=alert_id"""
        """exa_json_path=$.actor,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
        """exa_json_path=$.business,exa_field_name=company"""
        """exa_json_path=$.org,exa_field_name=object"""
        """exa_json_path=$.action,exa_field_name=event_name"""
        """exa_json_path=$._document_id,exa_field_name=doc_id"""  
        """exa_json_path=$.repo_id,exa_field_name=resource_id"""                
    ]
    ParserVersion = "v1.0.0"


}
```