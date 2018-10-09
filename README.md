# SSL Expiry

A simple script to check the expiration date on a list of domains. This simple python 3 utility is meant to be deployed as a cron or run from a lambda service.

## Usage

Create a `python3.6` virtualenv and invoke the python script

```sh
virtualenv venv --python=python3.6
source venv/activate
echo "google.com\nfacebook.com" | python ssl_expiry.py
```
```
google.com cert is fine
facebook.com cert is fine
```

## Install the lambda function on AWS

```bash
npm i -g serverless
export AWS_PROFILE=your-aws-profile
sls deploy
```

## Invoke the lambda

```bash
sls invoke -f main --log
```

## License

[MIT](LICENSE.md) © [Lucas Roesler](https://lucasroesler.com/)
