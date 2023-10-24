#### Parser Content
```Java
{
Name = "ibm-s-leef-alert-trigger-success-ubamachinelearninganomaly"
Vendor = "IBM"
Product = "IBM Sense"
TimeFormat = "epoch"
Conditions = [
"""|IBM|Sense|"""
"""UBA Machine Learning Anomaly"""
]
Fields = [
"""usrName =({user}[\w\.\-]{1,40}\$?)\s"""
"""senseValue=({sense_value}\d+)\s"""
"""senseScore=({sense_score}[\d.]+)"""
"""startTime=({time}\d{13})"""
"""\|IBM\|Sense\|[\d.]+\|({alert_name}[^\|]+)\|"""
"""cat=({alert_type}.+\S)\s+src"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
]
ParserVersion = "v1.0.0"


}
```