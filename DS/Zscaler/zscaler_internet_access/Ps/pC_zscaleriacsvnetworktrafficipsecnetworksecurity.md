#### Parser Content
```Java
{
Name = zscaler-ia-csv-network-traffic-ipsecnetworksecurity
  ParserVersion = "v1.0.0"
  Conditions = [ """IPSEC",""" ]
  Fields = ${ZscalerWeakParsersTemplates.zscaler-ia-csv-events-1.Fields}[
    """\d\s\d\d:\d\d:\d\d\s\d\d\d\d","({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)""""
  ]

zscaler-ia-csv-events-1 = {
    Vendor = Zscaler
    Product = Zscaler Internet Access
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Fields = [
      """({time}\w{3}\s{1,2}\d{1,2} \d\d:\d\d:\d\d \d\d\d\d)"""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){4}"({dest_port}\d+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){5}"({src_port}\d+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){8}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){9}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){15}"({action}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){19}"({service_name}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){20}"({app}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){21}"({protocol}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){22}"({category}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){23}"({location}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){25}"({rule}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){26}"({bytes_in}\d+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){27}"({bytes_out}\d+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){28}"({duration}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){30}"({session_id}[^"]+)""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){31}"(None|({threat_category}[^"]+))""""
      """\d\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){34}"(NA|({src_host}[^"]+))""""
    
}
```