#### Parser Content
```Java
{
Name = "onelogin-o-cef-app-login-assumingactinguserid"
  ParserVersion = "v1.0.0"
  Vendor = "OneLogin"
  Product = "OneLogin"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """assuming_acting_user_id":""", """app_name":""", """user_name":""", """event_type_id":""", """destinationServiceName =OneLogin""" ]
  Fields = [
    """"created_at":\s*"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3}Z)""",
    """\WdestinationServiceName =({app}\w+)""",
    """"app_name":\s*"\s*({app}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"event_type_id":\s*({activity_code}\d+)""",
    """"actor_user_name":"({full_name}[^"]+?)\s*"""",
    """"ipaddr":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"notes":\s*"\s*({failure_reason}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"notes":\s*"\s*({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"custom_message":\s*"\s*({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"error_description":\s*"\s*({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"event_type_name":"({operation}[^"]+)"""",
    """"event_type_description":"({additional_info}[^"]+)"""",
    """"user_id":({user_id}\d+)""",
    """suser=(({user_id}\d+)|({email_address}[^@\s]+@[^\s\.]+\.[^\s]+))""",
    """duser=({dest_user}[^@\s]+@[^\s\.]+\.[^\s]+)"""
  ]
  DupFields = ["user_id->account"]


}
```