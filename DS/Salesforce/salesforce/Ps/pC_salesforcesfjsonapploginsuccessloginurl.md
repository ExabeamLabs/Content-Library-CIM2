#### Parser Content
```Java
{
Name = salesforce-sf-json-app-login-success-loginurl
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"LoginUrl":""","""sales""", """"LoginHistory"""", """LoginTime":""", """LoginType":""" ]
  Fields = [
    """exa_regex=({app}salesforce)""",
    """exa_json_path=$..LoginTime,exa_regex=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..Status,exa_field_name=result""",
    """exa_json_path=$..LoginType,exa_field_name=login_type_text""",
    """exa_json_path=$..Browser,exa_regex=(Unknown|({browser}[^"]+))""",
    """exa_json_path=$..UserId,exa_field_name=user_id"""
    """exa_json_path=$..Platform,exa_regex=(Unknown|({os}[^"]+))""",
    """exa_json_path=$..SourceIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.operationName,exa_field_name=operation"""
    """exa_json_path=$..AccountDisplayName,exa_field_name=full_name"""
    """exa_json_path=$..AccountId,exa_field_name=account_id"""
    """exa_json_path=$..ActivityType,exa_field_name=action"""
    """exa_json_path=$..CipherSuite,exa_field_name=cipher"""
    """exa_json_path=$..TlsProtocol,exa_field_name=protocol"""
    """exa_json_path=$.properties.City,exa_field_name=city"""
    """exa_json_path=$.properties.CountryCode,exa_field_name=country_code"""
  ]


}
```