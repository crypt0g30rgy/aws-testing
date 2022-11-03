## Pentesting an s3 Bucket
### List bucket
``aws s3 ls s3://*bucket*``

### Copy to bucket
``aws s3 cp poc s3://*bucket*``

### Remove from bucket
``aws s3 rm s3://*bucket*/test.txt``

### Search for a File
``aws s3 ls s3://your-bucket --recursive | grep your-search | cut -c 32-``

### Check bucket Size
``aws s3 ls --summarize --human-readable --recursive s3://*bucket*``

### Download bucket data
``aws s3 sync s3://*bucket* *local folder*``

### Miscelanious
``
aws s3api get-bucket-acl --bucket *bucket*``

``aws s3api get-object-acl --bucket  --key read-acp.txt ``

``aws s3api put-bucket-acl --bucket *bucket* --grant-full-control emailaddress=youremail@domain.tld && echo "success"``
