#### Parser Content
```Java
{
Name = amd-p-csv-network-notification-success-flowdelete
    Vendor = AMD
    Product = Pensando
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSZ"
    Conditions = ["""pen-netagent""","""flow_delete"""]
    Fields = [
       """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
       """\d{2}Z ({host}[\w.-]+?) pen-netagent""",
       """({event_name}flow_delete),({action}[^,]+),({vrf}\d+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_port}\d+),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_port}\d+),({protocol}\d+),({session_id}[^,]+),({policy_id}[^,]+?),({rule_id}\d+),({rule}[^,]+?),({packets}\d+),({bytes_in}\d+),({rflow_packets}\d+),({bytes_out}\d+),({vlan_id}\d+),({device_type}[^,]+),([^,]*?,){2}({mac}[^,]+?),"""
    ]


}
```