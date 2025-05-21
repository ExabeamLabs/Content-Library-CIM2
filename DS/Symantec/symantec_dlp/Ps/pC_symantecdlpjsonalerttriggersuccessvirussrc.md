#### Parser Content
```Java
{
Name = "symantec-dlp-json-alert-trigger-success-virussrc"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""type":""""
""","virusSrc":""""
""","virusName":""""
]
Fields = [
"""\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s"""
""""@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
""""srcHostname":"({src_host}[^"]+)"""
""""srcIP":"(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
""""virusSrc":"({alert_type}[^"]+)"""
""""filePath":"(Unavailable|({malware_url}[^"]+))"""
""""virusName":"({alert_name}[^"]+)"""
""""userID":"(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""action":"({action}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```