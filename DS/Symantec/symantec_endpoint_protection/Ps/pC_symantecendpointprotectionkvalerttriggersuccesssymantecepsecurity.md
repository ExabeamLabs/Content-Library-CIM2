#### Parser Content
```Java
{
Name = "symantec-endpointprotection-kv-alert-trigger-success-symantecepsecurity"
Conditions = [
"""vendor_product="Symantec Endpoint Protection""""
"""eventtype=symantec_ep_security"""
]
ParserVersion = "v1.0.0"

s-symantec-alert.Fields}[
    """Local_Host_IP_masked="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Remote_Host_IP_masked="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"
},
{
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
"""\sEnd_Time="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""\sHost_Name =({host}[^,]+?)\s*(,|$)"""
"""\sdest=({dest_host}[^,]+?)\s*(,|$)"""
"""\suser=({user}[^,]+?)\s*(,|$)"""
"""\saction=({action}[^,]+?)\s*(,|$)"""
"""\ssignature="({alert_name}[^"]+)"""
"""\seventtype="?({alert_type}[^",]+)"""
"""\sseverity=({alert_severity}[^,]+?)\s*(,|$)"""
"""\sEvent_Description="({additional_info}[^"]+)"""
"""\sdest_port=({dest_port}\d+)"""
"""orig_host=({src_host}.*?),\s\w+="""
"""orig_source="({process_path}[^"]+\\({process_name}[^"]+))""""
]
Name = "symantec-endpointprotection-kv-alert-trigger-success-symantecepproactive"
Conditions = [
"""vendor_product="Symantec Endpoint Protection""""
"""symantec_ep_proactive"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
"""\sEnd_Time="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""\sHost_Name =({host}[^,]+?)\s*(,|$)"""
"""\sdest=({dest_host}[^,]+?)\s*(,|$)"""
"""\suser=({user}[^,]+?)\s*(,|$)"""
"""\saction=({action}[^,]+?)\s*(,|$)"""
"""\ssignature="({alert_name}[^"]+)"""
"""\seventtype="?({alert_type}[^",]+)"""
"""\sseverity=({alert_severity}[^,]+?)\s*(,|$)"""
"""\sEvent_Description="({additional_info}[^"]+)"""
"""\sdest_port=({dest_port}\d+)"""
"""orig_host=({src_host}.*?),\s\w+="""
"""src_masked="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Local_Host_IP_masked="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""orig_source="({process_path}[^"]+\\({process_name}[^"]+))""""
]
Name = "symantec-endpointprotection-kv-alert-trigger-success-symantecepsecurity"
Conditions = [
"""vendor_product="Symantec Endpoint Protection""""
"""eventtype=symantec_ep_security"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
"""\sEnd_Time="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""\sHost_Name =({host}[^,]+?)\s*(,|$)"""
"""\sdest=({dest_host}[^,]+?)\s*(,|$)"""
"""\suser=({user}[^,]+?)\s*(,|$)"""
"""\saction=({action}[^,]+?)\s*(,|$)"""
"""\ssignature="({alert_name}[^"]+)"""
"""\seventtype="?({alert_type}[^",]+)"""
"""\sseverity=({alert_severity}[^,]+?)\s*(,|$)"""
"""\sEvent_Description="({additional_info}[^"]+)"""
"""\sdest_port=({dest_port}\d+)"""
"""orig_host=({src_host}.*?),\s\w+="""
"""orig_source="({process_path}[^"]+\\({process_name}[^"]+))""""
]
Name = "symantec-endpointprotection-kv-alert-trigger-success-symanteceprisk-1"
Conditions = [
"""vendor_product="Symantec Endpoint Protection""""
"""symantec_ep_risk"""
]
ParserVersion = "v1.0.0"
},

{
    Name = symantec-endpointprotection-csv-alert-trigger-success-threatnum
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """スキャンが開始されました""", """,スキャン ID:""" ]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d),スキャン ID:""",
      """スキャン ID:\s*({alert_id}\d+)""",
      """ユーザー 1:\s*(SYSTEM|({user}[^\s,]+))""",
      """IP アドレス:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """コンピュータ:\s*({src_host}[\w\-.]+)""",
      """,({alert_name}[^,]+),スキャン 完了:""",
      """グループ:\s*({malware_url}[^,]+)""",
      """脅威:\s*({threat_num}[^,]+)""",
      """感染:\s*({infection_num}[^,]+)""",
    ]
    DupFields = [ "alert_name->alert_type" 
}
```