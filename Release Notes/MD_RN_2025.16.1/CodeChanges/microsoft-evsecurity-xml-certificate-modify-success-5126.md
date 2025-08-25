# Code Changes for microsoft-evsecurity-xml-certificate-modify-success-5126 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | activity_id |  | ['<Data Name=(\'|")CAConfigurationId(\'|")>({activity_id}[^<]+)'] |
| edit_regex_field | hash_sha1 |  | ['<Data Name=(\'|")NewSigningCertificateHash(\'|")>({hash_sha1}[^<]+)'] |