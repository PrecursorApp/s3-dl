# s3-dl
Simple script to download files from an s3 bucket.

We mainly use this script to download jars from s3 when we deploy new code. We needed something with minimal dependencies--most other scripts depend on perl or python. This script only needs a base FreeBSD install and curl.

Offers very little in the way of configuration. It's short enough that you can fork and edit your own copy.

## Usage

Export AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY, then call the script with the bucket as the first argument and the key as the second argument. The contents will print to stdout.

Example:

```
$ export AWS_ACCESS_KEY_ID="AKIAIOSFODNN7EXAMPLE"
$ export AWS_SECRET_ACCESS_KEY="wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY"
$ ./s3-dl.sh my-bucket-name my/key/name > mykey.txt
```
