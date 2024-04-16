#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-scanning
  Conditions = [ """vendor_product="Symantec Endpoint Protection"""", """Somebody is scanning your computer""" ]
  Fields = ${SymantecParsersTemplates.s-symantec-alert.Fields}[
    """Local_Host_IP_masked="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Remote_Host_IP_masked="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"

s-symantec-alert = {
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\sEnd_Time="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
      """\sHost_Name =({host}[^,]+?)\s*(,|$)""",
      """\sdest=({dest_host}[^,]+?)\s*(,|$)""",
      """\suser=({user}[\w\.\-]{1,40}\$?)\s*(,|$)""",
      """\saction=({action}[^,]+?)\s*(,|$)""",
      """\ssignature="({alert_name}[^"]+)""",
      """\seventtype="?({alert_type}[^",]+)""",
      """\sseverity=({alert_severity}[^,]+?)\s*(,|$)""",
      """\sEvent_Description="({additional_info}[^"]+)""",
      """\sdest_port=({dest_port}\d+)""", 
    
}
```