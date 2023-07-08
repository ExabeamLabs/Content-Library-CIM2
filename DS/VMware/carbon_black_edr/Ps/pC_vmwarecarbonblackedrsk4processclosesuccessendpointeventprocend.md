#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-process-close-success-endpointeventprocend
  ParserVersion = "v1.0.0"
  Conditions = [ """requestClientApplication=""" , """"type":"endpoint.event.procend"""", """destinationServiceName =""", """"process_username":"""" ]

carbonblack-edr}{
  Name = vmware-carbonblackedr-sk4-endpoint-activity-apicall
  Product = Carbon Black EDR
  Conditions = [ """requestClientApplication=""" , """"type":"endpoint.event.apicall"""", """destinationServiceName =""", """"process_username":"""" ]
  ParserVersion = "v1.0.0"
},

{
  Name = vmware-carbonblackedr-kv-endpoint-activity-cbprotection
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Cb Protection event:""", """subtype="""", """type=""", """policy=""" ]
  Fields = [
    """({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
    """\stext="({additional_info}[^"]+)"""",
    """\stype="({operation}[^"]+)"""",
    """\ssubtype="({event_name}[^"]+)"""",
    """\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)"""",
    """\susername="(({domain}[^"\\]+)\\)?({user}[^"\\]+)"""",
    """\sip_address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\spolicy="+({policy_name}[^"]+)"""",

  ]
  ParserVersion = "v1.0.0"
},

${LMSMSParsersTemplates.cef-microsoft-app-activity}{
  Name = microsoft-azuremon-sk4-app-activity-recommendation
  Product = Azure Monitor
  Conditions = [ """destinationServiceName =Azure""", """"category":"Recommendation"""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity.Fields}[
# azure_event_hub_name is removed
# azure_impact_level is removed
# azure_impact_level is removed
    #"""\Wext_Properties_UserAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"properties".*?"UserAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
# azure_recommendations_category is removed
# azure_recommendations_category is removed
# azure_resource is removed
  ]
  ParserVersion = "v1.0.0"
},

${LMSMSParsersTemplates.cef-microsoft-app-activity}{
  Name = microsoft-azuremon-sk4-app-notification-resourcehealth
  Product = Azure Monitor
  Conditions = [ """destinationServiceName =Azure""", """"category":"ResourceHealth"""" ]
  ParserVersion = "v1.0.0"
},


{
  Name = vectra-cs-kv-network-session-success-ldap
  Vendor = Vectra
  Product = Vectra Cognito Stream
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """vectra_metadata_ldap""", """METADATA_LDAP""" ]
  Fields = [
    """ts="+({time}\d{13})""",
    """id.orig_h="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+"""
    """id.orig_p="+({src_port}\d+)"+""",
    """id.resp_h="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+""",
    """id.resp_p="+({dest_port}\d+)"+""",
    """orig_hostname="+({src_host}[^"]+)"+"""
    """resp_hostname="+(null|((IP-)*({dest_host}[^"]+)))""",
    """result_code="+({result}[^"]+)"+""",
    """uid="*({user}[^"\s]+)"""
  
}
```