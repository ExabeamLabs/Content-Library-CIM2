#### Parser Content
```Java
{
Name = proofpoint-tap-kv-email-receive-mailreceived
Vendor = Proofpoint
Product = Targeted Attack Platform
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ - ProofpointTAP - """
]
Fields = [
  """(delivery|block|click|message)Time="*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z"""
  """- ProofpointTAP -\s+({result}[^\s-]+)\s+"""
  """({alert_name}ProofpointTAP)"""
  """\sGUID="*({alert_id}[^\s"]+)"""
  """- ProofpointTAP -\s+CLKBLK\s+-.*?\smessageID=({alert_id}\S+)"""
  """\srecipient="*({dest_email_address}[^\s"]+)"""
  """\ssender="*(null|({src_email_address}[^\s"]+))"""
  """\ssenderIP="*(null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\sthreatsInfoMap=\[\{.+?,({alert_type}.+?)\}"""
  """\sthreatsInfoMap="*\[\{.+?,\\"*classification\\"*:\\"*({alert_type}[^\\"]+)"""
  """\sclass=({alert_type}.+?)\s+\w+="""
  """\ssubject="({email_subject}[^"]+)"""
  """\smalwareScore="*({malware_score}\d+)"""
  """\sspamScore="*({spam_score}\d+)"""
  """\sphishScore="*({phishing_score}\d+)"""
  """\smessageSize="*({bytes}\d+)"""
]
DupFields = [
  "dest_email_address->email_recipients"
  "src_email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```