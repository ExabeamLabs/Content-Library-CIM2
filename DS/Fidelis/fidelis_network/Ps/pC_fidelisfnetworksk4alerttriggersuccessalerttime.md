#### Parser Content
```Java
{
Name = "fidelis-fnetwork-sk4-alert-trigger-success-alerttime"
Vendor = "Fidelis"
Product = "Fidelis Network"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""ALERT_TIME":""""
"""destinationServiceName =Fidelis"""
""""ACTION":"alert""""
]
Fields = [
""""ALERT_TIME\":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\""""
""""ALERT_ID\":"({alert_id}\d+)\""""
""""RULE_NAME\":"({rule}[^\"]+)\""""
""""PROTOCOL\":"({protocol}[^\"]+)\""""
""""FILE_NAME\":"({file_name}[^\"]+a)\""""
""""SRC_IP\":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
""""DEST_IP\":"({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
""""HOST_IP\":"({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
""""DEST_PORT\":"({dest_port}\d+)\""""
""""SRC_PORT\":"({src_port}\d+)\""""
""""SHA256\":"({hash_sha256}[^\"]+)\""""
""""SUMMARY\":"({additional_info}[^\"]+)\""""
""""SRC_COUNTRY_NAME\":"(?:unknown|({src_country}[^\"]+))\""""
""""DEST_COUNTRY_NAME\":"(?:unknown|({dest_country}[^\"]+))\""""
""""TARGET\":"({target}[^\"]+)\""""
""""FIDELIS_SCORE\":"({original_risk_score}\d+)\""""
""""ACTION\":"({alert_name}[^\"]+)\""""
""""FILE_TYPE\":"({file_type}[^\"]+)\""""
""""SEVERITY\":"({alert_severity}[^\"]+)\""""
""""SESSION_ID\":"({session_id}[^\"]+)\""""
"""\smsg=({additional_info}.+)\soldFilePath="""
""""APPLICATION_USER\":"(({email_address}[^@]+?@[^\"]+)|({user}[^\"]+?))\""""
""""MD5":"({hash_md5}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```