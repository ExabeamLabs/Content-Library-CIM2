#### Parser Content
```Java
{
Name = citrix-cvapps-json-vpn-session-success-sessionstart
  ParserVersion = v1.0.0
  Product =  Citrix Virtual Apps
  Conditions = [ """"occurrence_event_type":"Session.Logon"""", """"entity_type":"user"""", """"product":"Citrix Virtual Apps and Desktops"""" ]

citrix-json-virtual-apps {
    Vendor = Citrix
    Product = Citrix Virtual Apps
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields = [
      """exa_json_path=$.timestamp,exa_field_name=time""",
      """exa_json_path=$.occurrence_event_type,exa_field_name=event_name""",
      """exa_json_path=$.client_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
      """exa_json_path=$.device_id,exa_field_name=src_host""",
      """exa_json_path=$.domain,exa_field_name=domain""",
      """exa_json_path=$.entity_id,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """exa_json_path=$.session_user_name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """exa_json_path=$.user_name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """exa_json_path=$.user_upn,exa_field_name=user_upn""",
      """exa_json_path=$.os_name,exa_field_name=os""",
      """exa_json_path=$.browser_name,exa_field_name=browser""",
      """exa_json_path=$.city,exa_field_name=city""",
      """exa_json_path=$.country,exa_field_name=country""",
      """exa_json_path=$.app_name,exa_field_name=app""",
      """exa_json_path=$.server_name,exa_field_name=server_name""",
      """exa_json_path=$.tenant_id,exa_field_name=tenant_id""",
      """exa_json_path=$.event_id,exa_field_name=event_id""",
      """exa_json_path=$.event_type,exa_field_name=event_subtype""",
      """exa_json_path=$.event_category,exa_field_name=event_category""",
      """exa_json_path=$.event_source,exa_field_name=log_source""",
      """exa_json_path=$.product,exa_field_name=product_name""",
      """exa_json_path=$.transaction_id,exa_field_name=transaction_id""",
      """exa_json_path=$.os_version,exa_field_name=os_version""",
      """exa_json_path=$.event_status,exa_field_name=result""",
      """exa_json_path=$.policy_result,exa_field_name=result""",
      """exa_json_path=$.policy_name,exa_field_name=policy_name""",
      """exa_json_path=$.saas_app_launch_url,exa_field_name=url""",
      """exa_json_path=$.browser_version,exa_field_name=user_agent"""
    
}
```