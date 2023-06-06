#### Parser Content
```Java
{
Name = exabeam-aa-kv-alert-trigger-exaanalyticsmaster-1
    ParserVersion = v1.0.0
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """exabeam-analytics-master""", """Exabeam""", """ top_reasons="""", """ id="""", """ score="""" ]
    Fields = [ 
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\sexabeam-analytics-master""",
        """\sid="({session_id}[^"]+)"""",
        """\sscore="({original_risk_score}\d+)"""",
        """\suser="(\*+|({user}[^"]+))"""",
        """\surl="({url}[^"]+)"""",
        """\sstatus="({incident_status}[^"]+)""""
        """\ssrc_host="(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^"]+))"""",
        """\shost_name="({host}[^"]+)"""",
        """\sreasons_count="({reasons_count}\d+)""",
        """\stop_reasons="(|({top_reasons}[^"]*))\"*\s+\w+=""",
        """\szones="({network_zones}[^"]+)"""",
        """type="({category}[^"]+)"""",
        """top_users="({top_users}[^"]+)"""
    ]
  

}
```