#### Parser Content
```Java
{
Name = exabeam-aa-kv-alert-trigger-exaanalyticsmaster
  ParserVersion = v1.0.0
  Vendor = Exabeam
  Product = Advanced Analytics 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """exabeam-analytics-master""","""Exabeam""","""timestamp=""",""" id="""",""" score="""" ]
  Fields = [
    """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """event_code="({event_code}\d+)"""",
    """additional_info="\[({additional_info}[^"]+?)\]\s*"""",
    """\sid="({session_id}[^"]+)"""",
    """\sscore="({original_risk_score}\d+)"""",
    """\suser="(\*+|({user}[^"]+))"""",
    """\ssrc_host="(({src_ip}[a-fA-F:\d.]+)|({src_host}[^"]+))"""",
    """\shost="({host}[^"]+)"""",
    """\ssrc_ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\sevent_type="({event_category}[^"]+)"""",
    """\srule_id="({rule_id}[^"]+)"""",
    """\srule_name="({rule}[^"]+)"""",
    """\srule_description="({rule_description}[^"]+)"""",
    """\sdest_host="(({dest_ip}[a-fA-F:\d.]+)|({dest_host}[^"]+))"""",
    """\sdest_ip="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """\sexternal_domain="({external_domain}[^"]+)"""",
    """\ssender="({email_address}[^"]+)"""",
    """\sexternal_address="({external_address}[^"]+)"""",
    """\ssubject="({email_subject}[^"]+)"""",
    """\sdirection="({direction}[^"]+)"""",
    """\sfull_url="({url}[^"]+)"""",
    """\sweb_domain="({web_domain}[^"]+)"""",
    """\scategory="({category}[^"]+)"""",
# incident_start_time is removed
# incident_end_time is removed
    """\sstatus="({incident_status}[^"]+)""""
  ]


}
```