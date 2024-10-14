#### Parser Content
```Java
{
Name = airlock-allowlisting-json-app-activity-success-serveractivity
  Vendor = Airlock
  Product = Airlock Allowlisting
  TimeFormat = "dd/MM/yyyy HH:mm:ss a"
  ExtractionType = json
  Conditions = [ """"event":"ServerActivityMessage"""", """"user":"""", """"datetime":"""", """"task":"""" ]
  Fields = [
    """exa_json_path=$.datetime,exa_field_name=time""",
		"""exa_json_path=$.user,exa_regex=(SYSTEM|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """exa_regex=({event_name}ServerActivityMessage)""",
    """exa_json_path=$.task,exa_field_name=operation""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
  ]
  ParserVersion = "v1.0.0"


}
```