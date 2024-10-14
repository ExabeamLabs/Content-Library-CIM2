#### Parser Content
```Java
{
Name = saviynt-savy-json-app-activity-success-message
    Vendor = Saviynt
    Product = Saviynt
    ParserVersion = v1.0.0
    ExtractionType = json
    TimeFormat = "dd-MMM-yyyy HH:mm:ss"
    Conditions = [ """"ACTION TAKEN":""", """"ACCESSED BY":""", """"OBJECT TYPE":""", """"MESSAGE":""" ]
    Fields = [
      """exa_json_path=$.['EVENT TIME'],exa_field_name=time"""
      """exa_json_path=$.['ACTION TAKEN'],exa_field_name=operation"""
      """exa_json_path=$.EMAIL,exa_field_name=email_address"""
      """exa_json_path=$.['ACCESSED BY'],exa_field_name=user"""
      """exa_json_path=$.['FIRST NAME'],exa_field_name=first_name"""
      """exa_json_path=$.['LAST NAME'],exa_field_name=last_name"""
      """exa_json_path=$.MESSAGE,exa_field_name=additional_info""" 
      """exa_json_path=$.['IP ADDRESS'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]


}
```