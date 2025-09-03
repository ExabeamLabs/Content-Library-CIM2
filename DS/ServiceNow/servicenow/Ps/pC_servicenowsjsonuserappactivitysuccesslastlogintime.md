#### Parser Content
```Java
{
Name = servicenow-s-json-user-app-activity-success-lastlogintime
  Vendor = ServiceNow
  Product = ServiceNow
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions= [ """"sys_created_on":""", """"u_country":""", """"last_login_time":""" ]
  Fields =[
  	"""exa_json_path=$.sys_created_on,exa_field_name=time""",
  	"""exa_json_path=$.last_login_time,exa_field_name=additional_info""",
  	"""exa_json_path=$.u_country.display_value,exa_field_name=country_code""",
    """exa_json_path=$.user_name,exa_field_name=user"""
    """exa_json_path=$.active,exa_field_name=status_msg"""
    """exa_json_path=$.department.display_value,exa_field_name=department"""
    """exa_json_path=$.email,exa_field_name=email_address"""
  ]


}
```