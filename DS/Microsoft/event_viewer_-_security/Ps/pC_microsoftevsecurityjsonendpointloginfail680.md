#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-680"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [ """"event_id":680""", """"Logon attempt by:""" ]
Fields = [
"""exa_json_path=$.message,exa_regex=({event_name}Logon attempt)""",
"""exa_json_path=$.@timestamp,exa_field_name=time""",
"""exa_json_path=$.computer_name,exa_field_name=host""",
"""exa_json_path=$.event_data.param2,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.event_data.UserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.event_data.User,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.event_data.param3,exa_regex=^({dest_host}[\w\-.]+)$""",
"""exa_json_path=$.event_data.SourceWorkstation,exa_regex=^({dest_host}[\w\-.]+)$""",
"""exa_json_path=$.event_data.param4,exa_field_name=result_code""",
"""exa_json_path=$.event_data.ErrorCode,exa_field_name=result_code""",
"""exa_json_path=$.hostname,exa_field_name=domain""",
"""exa_json_path=$.user.identifier,exa_field_name=user_sid""",
"""exa_json_path=$.user.domain,exa_field_name=domain""",
"""exa_json_path=$.user.name,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.event_id,exa_field_name=event_code""",
"""exa_json_path=$.record_number,exa_field_name=event_id"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```