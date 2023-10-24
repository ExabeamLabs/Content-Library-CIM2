#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-alert-trigger-success-url-1
  Product = Singularity Platform
  Vendor = SentinelOne
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"url"""", """"i.scheme":"edr"""" ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """"event\.type":"({alert_name}[^"]+)"""
    """"event\.category":"({alert_type}[^"]+)"""",
    """"src\.process\.integrityLevel":"({alert_severity}[^"]+)""",
    """"endpoint\.name":"({host}[^"]+)"""
    """process\.name":"({process_name}[^"]+)""",
    """"endpoint\.os":"({os}[^"]+)"""
    """"agent\.version":\s*"+({user_agent}[^"]+)""""
    """"src\.process\.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))"""
    """"src\.process\.image\.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""
    """"src\.process\.image\.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""
    """"src\.process\.image\.md5":\s*\\?"+({hash_md5}[^"\\]+)"""
    """"src\.process\.pid":\s*({process_id}\d+)"""
    """"src\.process\.image\.path":"({process_path}({process_dir}[^"]+?)[\\\/]+({process_name}[^"\\\/]+))\\+"""",
    """"event\.id":"({alert_id}[^"]+)""",
    """"event\.url\.action":"({method}[^"]+)""",
    """"url\.address":"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)""""
    """"endpoint\.type":"({host_type}[^"]{1,2000})"""
  ]
  DupFields = [ "host->dest_host", "url->malware_url" ]


}
```