#### Parser Content
```Java
{
Name = osquery-o-json-app-activity-success-removed
  ParserVersion = "v1.0.0"
  Conditions = [ """"calendarTime":""",""""action":"removed"""",""""decorations":""",""""hostIdentifier":"""" ]

osquery-app-activity = {
  Vendor = Osquery
  Product = Osquery
  ExtractionType = json
  TimeFormat = "MMM dd HH:mm:ss yyyy 'UTC'"
  Fields = [
    """exa_regex="calendarTime":"\w{3}\s({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d\s\w+)""""
    """exa_json_path=$..hostname,exa_field_name=host"""
    """exa_json_path=$.destinationServiceName,exa_field_name=app"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.uid,exa_field_name=user_id"""
    """exa_json_path=$.protocol,exa_field_name=protocol"""
    """exa_json_path=$.cmdline,exa_field_name=process_command_line"""
    """exa_json_path=$.name,exa_field_name=additional_info"""
    """exa_json_path=$.snapshot[0].query,exa_field_name=db_query"""
  
}
```