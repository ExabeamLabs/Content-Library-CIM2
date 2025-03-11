#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4673-1"
Conditions = [ """"EventID":"4673"""", """A privileged service was called""" ]
ExtractionType = json
ParserVersion = "v1.0.0"

windows-events-2.Fields}[
       """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+Z)?\s*({host}[^\s]+)\s""",
       """"Computer"+:"+({host}[^"]+)""",
       """exa_json_path=$.log.jsonPayload.Computer,exa_field_name=host""",
       """exa_json_path=$.log.jsonPayload.privileges,exa_field_name=privileges"""
    
}
```