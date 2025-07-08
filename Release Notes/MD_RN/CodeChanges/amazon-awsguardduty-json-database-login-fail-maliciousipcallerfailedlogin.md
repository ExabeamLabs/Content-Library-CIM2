# Code Changes for amazon-awsguardduty-json-database-login-fail-maliciousipcallerfailedlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tags | ['"tags":\[({tags}.+"\})\]\}'] | ['"tags":\s*({tags}[^$]+?)\]', 'exa_regex="tags":\s*({tags}[^$]+?)\]'] |