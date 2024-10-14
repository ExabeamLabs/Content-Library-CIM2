#### Parser Content
```Java
{
Name = "trendmicro-cas-cef-alert-trigger-success-cas"
Vendor = "Trend Micro"
Product = "Trend Micro Cloud App Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""CEF:"""
"""|Trend Micro|CAS|"""
"""TrendMicroCasAffectedUser="""
"""|securityrisk|"""
]
Fields = [
"""\Wrt=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""CEF:([^\|]*\|){6}({alert_severity}[^\s]+)"""
"""\WdestinationServiceName =({app}.+?)\s\w+="""
"""\Wcat=({alert_type}.+?)\s\w+="""
"""\Wmsg=({additional_info}.+?)\s\w+="""
"""\Wcs2=(|({additional_info}.+?))\s\w+="""
"""\WTrendMicroCasAffectedUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+="""
"""\WTrendMicroCasAffectedUser=({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\.]+).+?)\s\w+="""
"""\WTrendMicroCasLocation=({malware_url}.+?)\s\w+="""
"""\Waction=({result}.+?)\s\w+="""
"""\Wfname=({file_name}.+?)\s\w+="""
"""\Wcs2=(|({alert_name}.+?))\s\w+="""
"""\Wcs1=(|({alert_name}.+?))\s\w+="""
]
ParserVersion = "v1.0.0"


}
```