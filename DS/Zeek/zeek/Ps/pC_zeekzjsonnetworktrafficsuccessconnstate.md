#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-success-connstate
  Vendor = Zeek
  Product = Zeek
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ 
""""id.orig_h"""
""""id.resp_h"""
""""conn_state"""
""""orig_pkts"""
]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.uid,exa_field_name=connection_id""",
    """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
    """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
    """exa_json_path=$.proto,exa_field_name=protocol""",
    """exa_json_path=$.orig_ip_bytes,exa_field_name=bytes_in""",
    """exa_json_path=$.resp_ip_bytes,exa_field_name=bytes_out""",
    """exa_json_path=$.sensorname,exa_field_name=sensor_name""",
    """exa_json_path=$.orig_pkts,exa_field_name=orig_pkts""",
    """exa_json_path=$.resp_pkts,exa_field_name=resp_pkts""",
    """exa_json_path=$.orig_cc,exa_field_name=country""",
    """exa_json_path=$.service,exa_field_name=operation"""
]


}
```