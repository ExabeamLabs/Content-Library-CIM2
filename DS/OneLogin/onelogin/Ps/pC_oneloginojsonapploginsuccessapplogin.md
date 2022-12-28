#### Parser Content
```Java
{
Name = onelogin-o-json-app-login-success-applogin
  ParserVersion = v1.0.0
  Vendor = OneLogin
  Product = OneLogin
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """assuming_acting_user_id":""", """app_name":""", """user_name":""", """event_type_id":""" ]
  Fields = [
    """"created_at":\s*"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3}Z)""",
    """"app_name":\s*"\s*({app}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"event_type_id":\s*({activity_code}\d+)""",
    """"user_name":\s*"({full_name}([^\\"]|(\\\\)*\\"|\\\\)+)"""",
    """"ipaddr":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"notes":\s*"({failure_reason}([^\\"]|(\\\\)*\\"|\\\\)+)"""",
    """"notes":\s*"({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+)"""",
    """"custom_message":\s*"({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+)"""",
    """"error_description":\s*"({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+)"""",
  ]
  DupFields = ["full_name->user"]


}
```