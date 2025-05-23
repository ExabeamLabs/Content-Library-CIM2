#### Parser Content
```Java
{
Name = exabeam-aa-kv-alert-trigger-exaanalyticsmaster
    ParserVersion = v1.0.0
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    event_timeFormat = "epoch"
    Conditions = ["""exabeam-analytics-master""", """Exabeam""", """timestamp=""", """ id="""", """ score=""""]
    Fields = [
      """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """event_code="({event_code}\d+)"""",
      """additional_info="\[({additional_info}[^"]+?)\]\s*"""",
      """\sid="({session_id}[^"]+)"""",
      """\sscore="({original_risk_score}\d+)"""",
      """\suser="\s*(\*+|(\w+-)?(\w+_)?\w+\.\.|(\w+?_)?(\w+-){1,2}\w+|((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))""",
      """\ssrc_host="(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^"]+))\s*"""",
      """\shost(_name)?="({host}[\w\-.]+)"""",
      """\ssrc_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """\sevent_type="({event_category}[^"]+)"""",
      """\srule_id="({rule_id}[^"]+)"""",
      """\srule_name="({rule}[^"]+)"""",
      """alert_name="({alert_name}[^"]+)"""
      """\srule_description="({rule_description}[^"]+)"""",
      """\sdest_host="(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+))"""",
      """\sdest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """\sexternal_domain="({external_domain}[^"]+)"""",
      """\ssender="({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """\ssubject="({email_subject}[^"]+)"""",
      """\sdirection="({direction}[^"]+)"""",
      """\sweb_domain="({web_domain}[^"]+)"""",
      """\scategory="({category}[^"]+)"""",
      # incident_start_time is removed
      # incident_end_time is removed
      """\sstatus="({incident_status}[^"]+)""""
      """\ssource="({log_source}[^"]+)"""",
      """user="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
      """action="({action}[^"]+)""""
      """\sreasons_count="({count}\d+)"""
      """\sevent_time="({event_time}\d{13})"""",
      """rule_description="({rule_usecases}[^"]+)""""
      """asset_labels="({asset_labels}[^"]+)"""
      """src_network_type="({src_zone}[^"]+)"""
    ]
  

}
```