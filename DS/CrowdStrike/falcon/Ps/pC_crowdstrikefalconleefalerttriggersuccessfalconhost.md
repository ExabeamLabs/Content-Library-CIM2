#### Parser Content
```Java
{
Name = "crowdstrike-falcon-leef-alert-trigger-success-falconhost"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LEEF:"""
"""|CrowdStrike|FalconHost|"""
]
Fields = [
"""\WscanResultName =(|({additional_info}.+?))\s*(\||\w+=|["\s]*$)"""
"""\Wdescription=(|({additional_info}.+?))\s*(\||\w+=|["\s]*$)"""
"""\Wurl=(|({url}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\Wsev=({alert_severity}\d+)"""
"""\WCrowdStrike\|(?:[^|]+\|){2}({alert_name}[^|]+)"""
"""\Wresource=(|({host}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WdevTime=({time}\d\d\d\d\-\d\d\-\d\d\s+\d\d\:\d\d\:\d\d)\s"""
"""\Wcat=(|({alert_type}.+?))\s*(\||\w+=|["\s]*$)"""
"""\Wdomain=(?:|N\/A|({domain}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WusrName =(|N\/A|({email_address}[^@=\|\s]+@[^"@\|\s=]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\||\w+=|["\s]*$)"""
"""\WscanResultDetected=(|({scan_result_detected}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WscanResultEngine=(|({scan_result_engine}[^=|\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WcommandLine=(|({process_command_line}.+?))\s*(\||\w+=|["\s]*$)"""
"""\Wmd5=(|({hash_md5}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\Wsha256=(|({hash_sha256}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\W(docAccessedFileName|fileName)=(|({file_name}.+?))\s*(\||\w+=|["\s]*$)"""
"""\W(docAccessedFilePath|filePath)=(|({file_path}.+?))\s*(\||\w+=|["\s]*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wproto=(|({protocol}[^=|\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WsrcPort=({src_port}\d+)"""
"""\WdstPort=({dest_port}\d+)"""
"""\WdnsRequestDomain=(|({dns_query}[^=|\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WrequestType=(|({dns_query_type}[^\s]+?))\s*(\||\w+=|["\s]*$)"""
"""\WfilePath=(|({process_path}[^\s]+\\+({process_name}[^\s]+)))"""
]
ParserVersion = "v1.0.0"


}
```