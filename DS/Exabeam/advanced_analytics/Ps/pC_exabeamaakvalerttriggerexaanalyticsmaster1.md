#### Parser Content
```Java
{
Name = exabeam-aa-kv-alert-trigger-exaanalyticsmaster-1
    ParserVersion = v1.0.0
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """exabeam-analytics-master""", """Exabeam""", """ id="""", """ score="""" ]
    Fields = [ 
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\sexabeam-analytics-master""",
        """\sid="({session_id}[^"]+)"""",
        """\sscore="({original_risk_score}\d+)"""",
        """\suser="(\*+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
        """\surl="({url}[^"]+)"""",
        """\sstatus="({incident_status}[^"]+)""""
        """\ssrc_host="(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^"]+))"""",
        """\shost_name="({host}[^"]+)"""",
        """\sreasons_count="({count}\d+)""",
        """\stop_reasons="(|({alert_reason}[^"]*))\"*\s+\w+=""",
        """\szones="({src_network_zone}[^"]+)"""",
        """type="({category}[^"]+)"""",
        """top_users="({top_users}[^"]+)"""
    ]
  

}
```