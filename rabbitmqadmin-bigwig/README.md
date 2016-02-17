[rabbitmqadmin](https://www.rabbitmq.com/management-cli.html), altered to work with [Bigwig](bigwig.io).

## Usage

Suppose your Bigwig provision ID is `$BIGWIG_ID`, and its AMQP username and password are `$BIGWIG_USER` and `$BIGWIG_PASS` respectively. Then you can, for example, list exchanges like this:

```
python2 rabbitmqadmin-bigwig \
  --host=bigwig.lshift.net \
  --port=443 \
  --path-prefix="/management/$BIGWIG_ID" \
  --username="$BIGWIG_USER" \
  --password="$BIGWIG_PASS" \
  --ssl \
  list exchanges
```

### What do you mean, provision ID?

If you go to the management interface, the URL should look like `https://bigwig.lshift.net/management/81547`. `81547` is the ID of the provision I was using.
