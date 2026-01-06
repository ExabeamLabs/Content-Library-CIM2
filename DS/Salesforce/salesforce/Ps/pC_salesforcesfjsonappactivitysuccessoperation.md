#### Parser Content
```Java
{
Name = salesforce-sf-json-app-activity-success-operation
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"operation":""", """"objectType":""", """"object":""", """"userName":""" ]
  Fields = [
    """exa_json_path=$.createdDate,exa_field_name=time""",
    """exa_json_path=$.employee.userName,exa_regex=^(Unavailable|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.operation.name,exa_field_name=operation"""
    """exa_json_path=$.transactionId,exa_field_name=transaction_id"""
    """exa_json_path=$.objectType.name,exa_field_name=object_type""",
    """exa_json_path=$.object.name,exa_field_name=object_name""",
    """exa_json_path=$.object.id,exa_field_name=object_id"""
  ]


}
```