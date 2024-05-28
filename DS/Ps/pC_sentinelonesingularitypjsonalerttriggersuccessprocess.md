#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-process"
Conditions = [
""""threatName":"""
""""classification": "Malware""""
""""agentComputerName":"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

sentinelone-activity.Fields} [
    """method:\s*"+({method}[^"]+)"""
    """url:\s*"+({url}(({protocol}[^:\\\/\s,"]+):\/*)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^\\\/\s:,"\?]+))({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?)"""

}
```