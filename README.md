[![Build Status](https://travis-ci.org/phstc/putsbox.svg)](https://travis-ci.org/phstc/putsbox)
[![Code Climate](https://codeclimate.com/github/phstc/putsbox/badges/gpa.svg)](https://codeclimate.com/github/phstc/putsbox)
[![Test Coverage](https://codeclimate.com/github/phstc/putsbox/badges/coverage.svg)](https://codeclimate.com/github/phstc/putsbox/coverage)

## PutsBox

PutsBox makes email integration tests easy. [Try it now](http://putsbox.com).


## Getting Started

For setting up PutsBox locally, please follow the [PutsReq Getting Started instructions](https://github.com/phstc/putsreq/blob/master/README.md#getting-started). With the difference that PutsBox needs [Inbound Email Parse Webhook](https://sendgrid.com/docs/API_Reference/Webhooks/inbound_email.html) configured for receiving emails.

### Production

In production (Heroku), PutsBox runs on mLab sandbox, with a storage of 500 MB. For avoiding getting exceeding the capacity, the `emails` collection must be converted into capped collections.

```
db.runCommand({ "convertToCapped": "emails",  size: 20000000 });
```

### License

Please see [LICENSE](https://github.com/phstc/putsbox/blob/master/LICENSE) for licensing details.