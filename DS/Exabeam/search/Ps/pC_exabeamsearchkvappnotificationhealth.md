#### Parser Content
```Java
{
Name = exabeam-search-kv-app-notification-health
    ParserVersion = "v1.0.0"
    Conditions = [""" Exabeam """, """exabeam-analytics-health"""]
    Fields = ${ExabeamDlParserTemplates.exabeam-system-health-alert.Fields} [
      """limeSyslogImporterHealthID="({additional_info}.+?)\s*"\s"*""",
      """user":"(Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    ]
  
exabeam-system-health-alert {
    Vendor = Exabeam
    Product = Search
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """\d\d.\d\d\dZ\s+({event_name}[^\s]+)\s""",
      """app":"({app}[^"]+)""",
      """event_subtype":"({event_subtype}[^"]+)""",
      """src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """host":"({host}[^"]+)""",
      """activity":"({operation}[^"]+)""",
      """additional_info":"({additional_info}.+?)\s*"}}\s"*""",
      """exa_jdbc_database:({db_name}[^\\"\]]+)"""
      """"event_type":"({event_category}[^"]+)""""
    
}
```