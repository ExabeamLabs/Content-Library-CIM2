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
    Conditions = [ """"mhl":""",""""sa":""",""""pph":""",""""dp":""" ]
    Fields = [
        """"sa":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
        """"da":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
        """"sp":\s*({src_port}\d{1,9})\D""",
        """"dp":\s*({dest_port}\d{1,9})\D""",
        """"ibc":\s*({bytes_in}\d+)""",
        """"obc":\s*({bytes_out}\d+)""",
        """"pr":\s*({protocol}\d+)""",
        """"ct":\s*({connection_type}\d+)""",
        """"pa":\s*"(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
        """"pn":\s"({process_name}[^,]+)"""",
        """"pid":\s*({process_id}\d+)""",
        """"ppn":\s"({parent_process_name}\s*[^,]+)"""",
        """"ppid":\s*({parent_process_id}\d+)""",
        """"dh":\s*"({dest_host}[^,]+)"""",
        """"iid":\s*({interface_id}\d+)""",
        """"fst":\s*({flow_start_time}\d{13})""",
        """"fet":\s*({flow_end_time}\d{13})""",
        """"udid":\s*"({udid}[^,]+)"""",
        """"liuid":\s*"(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
        """"ppath":\s*"({process_path}[^,]+)"""",
        """"pppath":\s*"({parent_process_path}[^,]+)""""
     ]
  

}
```