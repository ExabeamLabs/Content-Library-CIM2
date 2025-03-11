#### Parser Content
```Java
{
Name = zscaler-ia-csv-dns-request-fail-dnsblock
  ParserVersion = "v1.0.0"
  Conditions = [ ""","DNS_Block",""", ""","Block",""", ""","REQ_BLOCKED",""" ]
  Fields = ${ZscalerWeakParsersTemplates.zscaler-ia-csv-events-2.Fields}[
    """ \d\d:\d\d:\d\d \d\d\d\d","({location}[^"\-]+)"""
    """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",)"({department}[^"\-]+)"""
  ]

zscaler-ia-csv-events-2 = {
    Vendor = Zscaler
    Product = Zscaler Internet Access
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Fields = [
      """({time}\w{3}\s{1,2}\d{1,2} \d\d:\d\d:\d\d \d\d\d\d)"""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){3}"({action}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){4}"({result}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){5}"({rule}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){7}"({dns_query_type}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){8}"({dns_query}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){9}"({dns_response}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){10}"({dest_port}\d+)""""
      """\d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){13}"(8.8.8.8|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){12}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){14}"({categories}[^"]+)""""
      """ \d\d:\d\d:\d\d \d\d\d\d",("[^"]*",){15}"((?i)na|({src_host}[^"]+))""""   
    
}
```