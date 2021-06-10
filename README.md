# wordpress-to-mail

Publishes Worrdpress news via mail by reading from its feed URL.

## Get Started

Configure the tool via environment variables, then run the binary:

```
# Feed to get data from
export FEED_ADDRESS=https://opencast.org/feed/

# Mail server details
export MAIL_SENDER=news@example.com
export MAIL_RECEIVER=list@example.com
export MAIL_HOST=smtp.example.com
export MAIL_PASSWORD=secret

# If just one mail should be sent (1)
# or if all unsent mails should be sent at one (0)
export SEND_ONE=1

./wordpress-to-mail
```

Already processed posts are stored in `processed.yml` to avoid sending them twice:

```yml
- http://opencast.org/?p=898
- http://opencast.org/?p=894
```
