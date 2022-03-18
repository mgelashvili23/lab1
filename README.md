import boto3
session = boto3.Session(aws_access_key_id='access_key',
aws_secret_access_key='secret_key')
s3 = session.resource('s3')
for bucket in s3.buckets.all():
        print(bucket.name+"\n")






s3 = boto3.resource('s3')
for bucket in s3.buckets.all():
     if bucket.name.startswith('prod'): 
         print(bucket.name)

