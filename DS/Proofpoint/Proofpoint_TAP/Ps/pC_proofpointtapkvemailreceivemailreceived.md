#### Parser Content
```Java
{
Name = proofpoint-tap-kv-email-receive-mailreceived
Vendor = Proofpoint
Product = Proofpoint TAP
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
  """\ssender="*(null|({email_address}[^\s"]+))"""
  """\ssenderIP="*(null|({src_ip}[a-fA-F\d.:]+))"""
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
  "email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```