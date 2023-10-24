#### Parser Content
```Java
{
Name = "blackberry-c-json-alert-trigger-success-cylancescore"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = "M/d/yyyy H:mm:ss a"
Conditions = [
""""Cylance Score""""
""""PUP - """
""""Tenant""""
]
Fields = [
""""Access Time"+\s*:\s*"+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))"+\s*[,\]\}]"""
""""Date"+\s*:\s*"+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))"+\s*[,\]\}]"""
""""Device\s?Name"+\s*:\s*"+({host}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""Classification"+\s*:\s*"+({alert_name}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""Classification"+\s*:\s*"+({alert_type}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""File Owner"+\s*:\s*"+((N/A)|(({domain}[^\\]+)\\+({user}[\w\.\-]{1,40}\$?)))"+\s*[,\]\}]"""
""""Cylance Score"+\s*:\s*"+({alert_severity}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""File Path"+\s*:\s*"+({file_dir}([^"\\]|(\\\\)*\\"|\\[^"])+)\\+({file_name}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""File Path"+\s*:\s*"+({file_path}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""File Name"+\s*:\s*"+({file_name}([^"\\]|(\\\\)*\\"|\\[^"])+)"+\s*[,\]\}]"""
""""Description"+\s*:\s*"+(N/A|({alert_name}([^"\\]|(\\\\)*\\"|\\[^"])+))"+\s*[,\]\}]"""
""""({hash_type}MD5)"+\s*:\s*"+({old_hash}[0-9A-Za-z]+)"+\s*[,\]\}]"""
""""({hash_type}SHA256)"+\s*:\s*"+({old_hash}[0-9A-Za-z]+)"+\s*[,\]\}]"""
]
DupFields = [
"host->src_host"
"old_hash->new_hash"
]
ParserVersion = "v1.0.0"


}
```