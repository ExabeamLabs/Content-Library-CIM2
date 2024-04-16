#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-security"
Conditions = [
""""threatName":"""
""""classification": "Trojan""""
""""agentComputerName":"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

sentinelone-activity.Fields} [
    """method:\s*"+({method}[^"]+)"""
    """url:\s*"+({url}(({protocol}[^:\\\/\s,"]+):\/*)?({web_domain}[^\\\/\s:,"\?]+)(:({dest_port}\d+))?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?)"""

}
```