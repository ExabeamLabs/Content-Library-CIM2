#### Parser Content
```Java
{
Name = splunk-ses-kv-app-activity-searchname
  Vendor = Splunk
  Product = Splunk ES
  ParserVersion = "v1.0.0"
  TimeFormat = ["epoch_sec","epoch","MM/dd/yyyy HH:mm:ss"]
  occured_timeFormat = "yyyy-MM-dd"
  trigger_timeFormat = "epoch_sec"
  start_timeFormat = "epoch_sec"
  end_timeFormat = "epoch_sec"
  Conditions = [ """search_name="""", """info_max_time="""", """info_min_time="""", """info_search_time=""""  ]
  Fields = [
    """info_search_time="({time}\d{10})""",
    """nt_host="(NULL|({host}[\w\-.]+))"""",
# search_name is removed
# asset_priority is removed
    """dst_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# ics_tactic_name is removed
# ics_technique_id is removed
# ent_tactic_name is removed
# ent_technique_id is removed
    """orig_event_id="({event_id}[^"]+)"""",
    """src_city="(NULL|({city}[^"]+))""""
    """\ssearch_name="({alert_name}[^,"]+)",""",
    """\sIncident\sID="({alert_id}[^,"]+)",""",
    """\sIncident\sName ="({alert_type}[^,"]+)",""",
    """\sIncident\sTime="({occured_time}\d\d\d\d-\d\d-\d\d)",""",
    """\sIncident\sURL="({threat_url}[^,"]+)",""",
    """\sinfo_max_time="({end_time}\d{10})",""",
    """\sinfo_min_time="({start_time}\d{10})""",
    """\sinfo_search_time="({trigger_time}\d{10})""",
    """\sseverity="({alert_severity}[^,"]+)","""
   ]


}
```