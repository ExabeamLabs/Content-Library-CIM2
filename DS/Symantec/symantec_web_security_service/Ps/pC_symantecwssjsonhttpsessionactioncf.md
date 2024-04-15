#### Parser Content
```Java
{
Name = "symantec-wss-json-http-session-actioncf"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""filter_result_CF"""
"""action_CF"""
"""BlueCoat_CL"""
]
Fields = [
""""TimeGenerated"+:"+({time}[^"]+)"+,"""
""""Computer"+:"+({host}[^"]+)"+,"""
""""user_CF"+:"+(-|({user}[^"]+))"+,"""
""""user_agent_CF"+:"+(-|({user_agent}[^"]+))"+,"""
""""country_CF"+:"+(None|({country}[^"]+))"+,"""
""""app_CF"+:"+(none|({app}[^"]+))"+,"""
""""src_CF"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+,"""
""""action_CF"+:"+(-|({proxy_action}[^"]+))"+,"""
""""method_CF"+:"+({method}[^"]+)"+,"""
""""status_CF"+:"+({http_response_code}\d+)"+,"""
""""uri_query_CF"+:"+(-|({uri_query}[^"]+))"+,"""
""""url_CF"+:"+(-|({url}[^"]+))"+,"""
""""filter_result_CF"+:"+(-|({action}[^"]+))"+,"""
""""protocol_CF"+:"+(-|({protocol}[^"]+))"+,"""
""""bytes_sent_CF"+:"+(-|({bytes_out}\d+))"+,"""
""""bytes_recieved_CF"+:"+(-|({bytes_in}\d+))"+,"""
""""dport_CF"+:"+(-|({dest_port}\d+))"+,"""
""""proxy_ip_CF"+:"+(-|({proxy_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))"+,"""
""""_ResourceId"+:"+(-|({resource_id}[^"]+))"+,"""
""""Type"+:"+(-|none|({category}[^"]+))"+,"""
""""categories_CF"+:"+({category}[^"]+)""""
""""content_type_CF"+:"+(-|({mime}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```