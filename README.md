# tekton-set-commit-status
Set commit status to github, gitlab and ~~bitbucket~~
TODO: bitbucket

1. EventListener is filtering for push and merge hooks
2. Provide a secret in form:
```
apiVersion: v1
kind: Secret
metadata:
  name: git-token
type: Opaque
stringData:
  token: |-
    {
      "github": "token for github",
      "gitlab": "token for gitlab",
      "bitbucket": ""
    }
```
3. tekton url is hardcoded, can be moved to config map...
4. description within pipeline is hardcoded as well, not sure what should go there
