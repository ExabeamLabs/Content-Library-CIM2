#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-alert-trigger-success-url-1
  ExtractionType = json
  Product = Singularity Platform
  Vendor = SentinelOne
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"url"""", """"event.type":""" ]
  Fields = [    
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.['event.type'],exa_field_name=alert_name""",
    """exa_json_path=$.['event.category'],exa_field_name=alert_type""",
    """exa_json_path=$.['src.process.integrityLevel'],exa_field_name=alert_severity"""
    """exa_json_path=$.['endpoint.name'],exa_field_name=host""",
    """exa_json_path=$.['process.name'],exa_field_name=process_name""",
    """exa_json_path=$.['endpoint.os'],exa_field_name=os""",
    """exa_json_path=$.['agent.version'],exa_field_name=user_agent""",
    """exa_regex="src.process.user":"*((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+?))""""
    """exa_json_path=$.['src.process.image.sha256'],exa_field_name=hash_sha256""",
    """exa_json_path=$.['src.process.image.sha1'],exa_field_name=hash_sha1""",
    """exa_json_path=$.['src.process.image.md5'],exa_field_name=hash_md5""",
    """exa_json_path=$.['src.process.pid'],exa_field_name=process_id""",
    """exa_json_path=$.['src.process.image.path'],exa_regex=({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))$""",
    """exa_json_path=$.['event.id'],exa_field_name=alert_id""",
    """exa_json_path=$.['event.url.action'],exa_field_name=method""",
    """exa_json_path=$.['url.address'],exa_regex=({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)$""",
    """exa_json_path=$.['endpoint.type'],exa_field_name=host_type""",
  ]
  DupFields = [ "host->dest_host", "url->malware_url" ]


}
```