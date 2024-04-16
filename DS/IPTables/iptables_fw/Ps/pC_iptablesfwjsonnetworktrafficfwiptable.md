#### Parser Content
```Java
{
Name = iptables-fw-json-network-traffic-fwiptable
    ExtractionType = json
    ParserVersion = "v1.0.0"
    Vendor = IPTables
    Product = IPTables FW
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"logT":"FW-IPTables"""" ]
    Fields = [
      """exa_json_path=$.host,exa_field_name=host""",
      """exa_json_path=$.@timestamp,exa_field_name=time""",
      """exa_json_path=$.message,exa_regex=\sIN=({src_interface}[^=]+?)\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sOUT=({dest_interface}[^=]+?)\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sMAC=({src_mac}[^=]+?)\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sSRC=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sDST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sPROTO=({protocol}[^=]+?)\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sSPT=({src_port}\d+)\s+(\w+=|\\n")""",
      """exa_json_path=$.message,exa_regex=\sDPT=({dest_port}\d+)\s+(\w+=|\\n")""",
    ]
  

}
```