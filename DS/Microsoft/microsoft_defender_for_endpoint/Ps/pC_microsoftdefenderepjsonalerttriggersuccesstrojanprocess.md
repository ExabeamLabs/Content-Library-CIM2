#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-alert-trigger-success-trojanprocess"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""threatname":""""
""""scepmaldetecttime":""""
]
Fields = [
""""username":"({user_id}[^"]+)"""
""""threatname":"({alert_name}[^"]+)"""
""""threatid":({threat_id}\d+)"""
""""targethost":"({src_host}[^"]+)"""
""""severityid":({alert_severity}\d+)"""
""""scepmaldetecttime":"({time}[^"]+)"""
""""process":"({process_path}({process_dir}[^"]*?)({process_name}[^"\\\/]+))""""
""""path":"({malware_url}[^"]+)"""
""""ntdomain":"({domain}[^"]+)"""
""""name":"({alert_type}[^"]+)"""
""""maliciousfilect":({malicious_file_count}\d+)"""
""""mal_id":({malware_id}\d+)"""
""""executionstatus":({execution_status}\d+)"""
""""errorcode":\-?({error_code}\d+)"""
""""cleanaction":"({result}[^"]+)"""
""""category":"({threat_category}[^"]+)"""
""""actionsuccess":({result}[^,]+)"""
""""@version":"({version}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```