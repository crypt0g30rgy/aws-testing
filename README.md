# Find AWS keys
use the following regex;

## Access Key

``
grep -RP '(?<![A-Z0-9])[A-Z0-9]{20}(?![A-Z0-9])' *
``

## Secret Key

``
grep -RP '(?<![A-Za-z0-9/+=])[A-Za-z0-9/+=]{40}(?![A-Za-z0-9/+=])' *
``

# Configure new profile

``
aws configure --profile test
``

# Use new profile

``
aws --profile test
``

i.e 

``
aws --profile test s3 ls
``

# cognitocreds.py
A python script for testing Aws Cognito IdentityPoolId.

https://github.com/andresriancho/enumerate-iam

#Installation
Clone this repo; 
              
              git clone https://github.com/g30rgyth3d4rk/cognitocreds.git
#Requirements

``cd into cognitocreds``

``pip install boto3 or pip install -r requirement.txt``

#Usage

``python3 cognitocreds.py "region" "IdentityPoolId"``

i.e 

``python3 cognitocreds.py "us-west-2" "us-west-2:XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX"``
