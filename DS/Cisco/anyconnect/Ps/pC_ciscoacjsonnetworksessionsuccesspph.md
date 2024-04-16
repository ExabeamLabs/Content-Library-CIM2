#### Parser Content
```Java
{
Name = cisco-ac-json-network-session-success-pph
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = AnyConnect
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  flow_start_timeFormat = ["epoch"]
  flow_end_timeFormat = ["epoch"]
  ExtractionType = json
  Conditions = [ """"mhl":""",""""sa":""",""""pph":""",""""dp":""" ]
  Fields = [
      """exa_json_path=$.sa,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.da,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_json_path=$.sp,exa_field_name=src_port"""
      """exa_json_path=$.dp,exa_field_name=dest_port"""
      """exa_json_path=$.ibc,exa_field_name=bytes_in"""
      """exa_json_path=$.obc,exa_field_name=bytes_out"""
      """exa_json_path=$.pr,exa_field_name=protocol"""
      """exa_json_path=$.ct,exa_field_name=connection_type"""
      """exa_regex="pa":\s*"(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
      """exa_json_path=$.pn,exa_field_name=process_name"""
      """exa_json_path=$.pid,exa_field_name=process_id"""
      """exa_json_path=$.ppn,exa_field_name=parent_process_name"""
      """exa_json_path=$.ppid,exa_field_name=parent_process_id"""
      """exa_json_path=$.dh,exa_field_name=dest_host"""
      """exa_json_path=$.iid,exa_field_name=interface_id"""
      """exa_json_path=$.fst,exa_field_name=flow_start_time"""
      """exa_json_path=$.fet,exa_field_name=flow_end_time"""
      """exa_json_path=$.udid,exa_field_name=udid"""
      """exa_regex="liuid":\s*"(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
      """exa_json_path=$.ppath,exa_field_name=process_path"""
      """exa_json_path=$.pppath,exa_field_name=parent_process_path"""
    ]


}
```