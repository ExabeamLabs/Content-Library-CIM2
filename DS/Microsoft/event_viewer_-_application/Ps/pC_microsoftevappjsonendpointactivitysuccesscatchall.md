#### Parser Content
```Java
{
Name = microsoft-evapp-json-endpoint-activity-success-catchall
  ParserVersion = v1.0.0
  Product = Event Viewer - Application
  Conditions = [ """"EventID":""", """"Channel":"Application"""", """"ProviderName":"""" ]
  Fields = ${WindowsParsersTemplates.microsoft-json-events.Fields}[
    """exa_json_path=$.Computer,exa_field_name=host"""
		"""exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
		"""exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s"""
    """exa_regex=Account Domain:\s+({domain}[^\s]+)"""
    """exa_json_path=$.StringInserts,exa_regex=(\[\]|.+?"({additional_info}[^"]+))"""
  ]


}
```