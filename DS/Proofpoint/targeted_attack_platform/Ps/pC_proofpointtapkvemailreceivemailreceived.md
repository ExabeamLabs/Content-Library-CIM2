#### Parser Content
```Java
{
Name = proofpoint-tap-kv-email-receive-mailreceived
Vendor = Proofpoint
Product = Targeted Attack Platform
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
  """ - ProofpointTAP - """
]
Fields = [
  """(delivery|block|click|message)Time="*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z"""
  """- ProofpointTAP -\s+({result}[^\s-]+)\s+"""
  """({alert_name}ProofpointTAP)"""
  """\sGUID="*({alert_id}[^\s"]+)"""
  """- ProofpointTAP -\s+CLKBLK\s+-.*?\smessageID=({alert_id}\S+)"""
  """\srecipient="*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\ssender="*(null|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
  """\ssenderIP="*(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\sthreatsInfoMap=\[\{.+?,({alert_type}.+?)\}"""
  """\sthreatsInfoMap="*\[\{.+?,\\"*classification\\"*:\\"*({alert_type}[^\\"]+)"""
  """\sclass=({alert_type}.+?)\s+\w+="""
  """\ssubject="({email_subject}[^"]+)"""
  """\smalwareScore="*({malware_score}\d+)"""
  """\sspamScore="*({spam_score}\d+)"""
  """\sphishScore="*({phishing_score}\d+)"""
  """\smessageSize="*({bytes}\d+)"""
  """eventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
]
DupFields = [
  "dest_email_address->email_recipients"
]
ParserVersion = "v1.0.0"


}
```