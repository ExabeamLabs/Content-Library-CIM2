#### Parser Content
```Java
{
Name = "exabeam-aa-json-app-activity-success-search"
Conditions = [
  """"Exabeam Audit Event"""
  """"event_type":"app-activity""""
  """"activity":"Threat hunter search""""
  """"app":"Exabeam Advanced Analytics"""
]
ParserVersion = "v1.0.0"

SSSZ"
        Fields = [
            """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
            """\d\d.\d\d\dZ\s+({event_name}[^\s]+)\s""",
            """app":"({app}[^"]+)""",
            """event_subtype":"({event_subtype}[^"]+)""",
            """src_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
            """user":"(Unknown|({user}[^"]+))""",
            """host":"({host}[^"]+)""",
            """activity":"({operation}[^"]+)""",
            """additional_info":"({additional_info}.+?)\s*"}}\s"*""",
            """exa_jdbc_database:({db_name}[^\\"\]]+)"""
        
}
```