```
~/go/bin/gobench -u https://CFEEEB67E36ED362790B842F1C14A0F4.sk1.beta.us-west-2.clusters.wesley.amazonaws.com:443/api/v1?timeout=32s -c 1 -t 5 --auth "Bearer "
```

```
# 
~/go/bin/gobench -u https://CFEEEB67E36ED362790B842F1C14A0F4.sk1.beta.us-west-2.clusters.wesley.amazonaws.com:443/api/v1?timeout=32s -c 500 -t 5 --auth "Bearer "

# 
TOKEN=$(aws-iam-authenticator token --cluster-id eks-2021090810-onionq2aa7uq | jq -r .status.token)

# 
curl -k -v -XGET 'https://CFEEEB67E36ED362790B842F1C14A0F4.sk1.beta.us-west-2.clusters.wesley.amazonaws.com:443/api/v1?timeout=32s' \
-H "authorization: Bearer ${TOKEN}"
```