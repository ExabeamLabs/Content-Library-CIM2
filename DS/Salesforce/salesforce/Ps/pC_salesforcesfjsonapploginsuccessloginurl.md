#### Parser Content
```Java
{
Name = salesforce-sf-json-app-login-success-loginurl
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"LoginUrl":""","""salesforce.com"""", """LoginTime":""", """LoginType":""" ]
  Fields = [
    """exa_regex=({app}salesforce)""",
    """exa_json_path=$.LoginTime,exa_regex=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.Status,exa_field_name=result""",
    """exa_json_path=$.LoginType,exa_field_name=login_type_text""",
    """exa_json_path=$.Browser,exa_regex=(Unknown|({browser}[^"]+))""",
    """exa_json_path=$.UserId,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.Platform,exa_regex=(Unknown|({os}[^"]+))""",
    """exa_json_path=$.Application,exa_field_name=protocol""",
    """exa_json_path=$.SourceIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```