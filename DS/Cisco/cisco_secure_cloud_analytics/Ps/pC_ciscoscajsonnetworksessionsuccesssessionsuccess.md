#### Parser Content
```Java
{
Name = cisco-sca-json-network-session-success-sessionsuccess
  Vendor = Cisco
  Product = Cisco Secure Cloud Analytics
  TimeFormat = "yyyy-MM-dd HH:mm:ss" 
  flow_start_timeFormat = ["yyyy-MM-dd HH:mm:ss"]
  flow_end_timeFormat = ["yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """"connected_ipv6":""", """"netid":""", """"octets_in":""", """"profile_tag":""" ] 
  Fields = [
        """"start_timestamp_utc":\s*"*({flow_start_time}\d\d\d\d-\d+-\d+\s\d+:\d+:\d+)""""
	""""end_timestamp_utc":\s*"*({flow_end_time}\d\d\d\d-\d+-\d+\s\d+:\d+:\d+)""""
	""""port":\s*({src_port}\d{1,9})\D"""
        """"connected_port":\s*({dest_port}\d{1,9})\D"""
        """"protocol":\s*({protocol}\d+)"""
        """"octets_in":\s*({bytes_in}\d+)"""
        """"octets_out":\s*({bytes_out}\d+)"""	
	""""packets_in":\s*({packets_in}\d+)"""
	""""packets_out":\s*({packets_out}\d+)"""
	""""first_direction":\s*({direction}\d+)"""
        """"profile_tag":\s*"({additional_info}[^"]+)""""
        """"flags":\s*({tcp_flags}[^"]+)"""
	""""device_id":\s*({device_id}\d+)"""
	""""ipv6":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
	""""connected_ipv6":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
        """({bytes_unit}(?i)octets)"""
  ]
  DupFields = [ "flow_start_time->time" ]
  ParserVersion = "v1.0.0"


}
```