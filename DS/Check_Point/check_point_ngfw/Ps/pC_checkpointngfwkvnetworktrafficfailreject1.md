#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-fail-reject-1
  Conditions = [ """CheckPoint""", """action:"Reject"""", """ifdir:"""", """product:"Application Control"""" ]
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Fields = [
    """time:"({time}\d{10})"""
    """action:"({action}[^"]+)"""
    """({host}[^\s]+)\saction\:"Reject"""
    """ifdir"?:"({direction}\w+[^"])"""
    """origin:"({origin_ip}[^"]+)"""
    """appi_name:"({app}[^"]+)""""
    """cu_rule_category:"({rule_type}[^"]+)"""
    """dst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """event_name:"({event_name}[^"]+)"""
    """matched_category:"({category}[^"]+)"""
    """originsicname:"CN=({origin_name}[^",]+)"""
    """origin_sic_name:"CN=({origin_name}[^",]+)"""
    """product:"({product_name}[^"]+)"""
    """proto:"?({protocol}\d+)"""
    """service:"?({dest_port}\d+)"""
    """severity:"?({severity}\d+)"""
    """src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)"""
    """src_machine_name"?:"({src_host}[^"]+)"""
    """src_machine_name"?:"({src_host}[^"@]+)@({domain}[^"]+)"""
] 


}
```