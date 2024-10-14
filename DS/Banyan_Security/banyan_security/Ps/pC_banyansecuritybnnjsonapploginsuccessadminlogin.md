#### Parser Content
```Java
{
Name = banyansecurity-bnn-json-app-login-success-adminlogin
  ParserVersion = "v1.0.0"
  Conditions = [ """"type":""", """"AdminLogin"""", """"action":""", """"Grant"""" ]

banyan-events  = {
    Vendor = Banyan Security
    Product = Banyan Security
    ExtractionType = json
    TimeFormat = "epoch_sec"
    Fields = [
      """exa_json_path=$.created_at,exa_field_name=time""",
      """exa_regex=host_name":\s*"({dest_host}[^":]+)""",
      """exa_json_path=$.reported_by.host_ip,exa_regex=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
      """exa_json_path=$..client.ip_address,exa_regex=^(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)$"""
      """exa_regex="user":\s*\{[^\{\}]*?"name":\s*"({full_name}[^"]+)"""
      """exa_json_path=$..user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_json_path=$.type,exa_field_name=event_category""",
      """exa_json_path=$.sub_type,exa_field_name=operation_type""",
      """exa_json_path=$.action,exa_field_name=operation""",
      """exa_json_path=$..roles,exa_regex=\[({access}[^\]]+)"""
      """exa_json_path=$..groups,exa_regex=\[({group_info}[^\]]+)"""
      """exa_json_path=$.message,exa_field_name=additional_info""",
      """exa_json_path=$..user_agent,exa_field_name=user_agent"""
    
}
```